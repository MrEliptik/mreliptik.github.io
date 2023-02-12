---
title: "Get collision points of Areas in Godot"
layout: post
date: 2023-02-09 08:00
image: /assets/images/godot_area_collision/godot_area_collision.jpg
headerImage: true
tag:
- gamedev
- godot
- godot_3
category: blog
author: mreliptik
hidden: true # don't count this post in blog pagination
description: Let me show you how to get the collision points between two Areas (2D and 3D)
---

In this blogpost, I'll show you how to get the collision points between two Areas (2D and 3D) in Godot 3.X. I'm specifying Godot 3 because it might be easier in 4, I don't know. 

First, I'll tell you why I wanted to do that. If you don't care, you can directly go to [The solution](#the-solution).

### The problem

In VR, you have to put your UI somewhere in the 3D world and you use an Area to interact with it, usually using a raycast. The raycast gives you the collision point so you can create a fake mouse event on the Control nodes of your UI. If you want to be able to "touch" the UI with your finger when using hand tracking, using a raycast doesn't work well. So instead, I attached an area to the fingertip. The only problem with this solution is that we have no way of knowing were exactly we collided with the UI's area. 

![VR UI interaction][vr_ui]

Well, of course there's a solution but what I mean is it's not available straight in the Area node. Enough talking, let's jump to the solution!


### The solution

Let's start with 2D as the solution is a bit simpler.

#### 2D

You can use the `collide_and_get_contacts` method available on [Shape2D][shape_2D]. To put it in context, let's say you have the `area_shape_entered(area_rid: RID, area: Area2D, area_shape_index: int, local_shape_index: int)` of one area connected to `on_area_shape_entered()`. As you can see in the signal we have the area_shape_index that we're going to use to get the shape from the area doing `var shape = area.shape_owner_get_owner(area_shape_index).shape` now that we have the shape of the area we're colliding with, we can use the method we saw earlier. 

{% highlight python %}

    func on_area_shape_entered(area_rid: RID, area: Area2D, area_shape_index: int, local_shape_index: int):
        var shape = area.shape_owner_get_owner(area_shape_index).shape
        var collision_points = $Area/CollisionShape.shape.collide_and_get_contacts(global_transform, shape, area.global_transform)

{% endhighlight %}

We simply provide the global transforms of the two areas and the shape we retrieved using `shape_owner_get_owner`.
The result is an `Array` with the collision points.

#### 3D

For 3D, we're going to basically do the same thing. The only different is that the class `Shape` doesn't have the same method as `Shape2D` to get the collision points. To achieve the same result, we'll query the `PhysicsServer`. 
Let's assume the same configuration as previously. In one of the area scene, we connect the signal `area_shape_entered` and we use the following code:

{% highlight python %}

    func on_area_shape_entered(area_rid: RID, area: Area2D, area_shape_index: int, local_shape_index: int):
        var area_space: RID = PhysicsServer.area_get_space(get_rid())
        var space_state: PhysicsDirectSpaceState = PhysicsServer.space_get_direct_state(area_space)
        var query: PhysicsShapeQueryParameters = PhysicsShapeQueryParameters.new()
        query.set_shape(area.shape_owner_get_owner(area_shape_index).shape)
        var collision_points: Array = space_state.collide_shape(query)

{% endhighlight %}

Let's break it down really quick.

First, we get the get the space in which the area resides. This is then used to get the space direct state that we store in `space_state`. This is going to be used to do the collision later on. 
Now it's time to construct the query with a `PhysicsShapeQueryParameters`. We only have to set_shape we want to use and for that, we use the same technique as in 2D, with `area.shape_owner_get_owner(area_shape_index).shape`.

The final line uses the `space_state` to collide the shape and get the collision points, in an `Array` 

And that's it! As you can see, when you know how to do it, it's not that hard! 

In my case, I simply calculate the average point between the collision points to know where to click on the UI in VR. 

Byyye ;)

[vr_ui]: /assets/images/godot_area_collision/vr_ui.png
[shape_2D]: https://docs.godotengine.org/en/stable/classes/class_shape2d.html