# Let's make our Green Box Rich

You must've seen in Mario games, that Mario goes around collecting coins. How do we make them in our game? First we create a new scene and a new node. The node type should be an ```Area 2D``` and taken from the ```+ Other Node``` option.

## Spriting the coins

Drag and drop the coin sprite from the assets to the scene. Centre it to the origin.<br>
Now add a collision shape to it. This time, CircleShape 2D fits our coin better. We'll need a new layer for the coins as it doesn't fall into the player, enemy or world category. The coin will only have to mask the player as it doesn't interact with anything else. Save the coin into a new folder. Let it be named "Objects". 

![coin](Images/coin.png)

### Adding a bit of bounce

Now we'll animate the coin so that it is a bit lively. For that we'll add a new node ```AnimationPlayer```. The animation window will come up in the bottom of the screen as well as some new icons in the top window. <br>
![animwin](Images/animwin.png)
![tools](Images/tools.png)

To animate the coin, click the animation menu and choose the new animation. Let's call it bouncing. <br>
A new timeline will have appeared on the animation window. That is a track and is used to change the properties (shown in the Inspector) of the object.

![track](Images/track.png)

To animate the object, we need to move the sprite and keyframe it (click on the key icon where we want to fix the extreme positions).

![anim1](Image/anim1.png) ![anim2](Image/anim2.png)

The above animation on being played will bounce the coin between these two places. There are more properties such as easing into extremes that can be experimented with.

### Dissappear after taking

Add a new animation using the animation menu. Let's call it "fading".
A new timeline will appear, one that will ignore the first animation.

In this one, instead of changing the position of the coin, we'll change the visibility of it. By changing the <b>A</b> value of the Modulate option, the coin's transperancy changes.

![visi](Images/visi.png) ![A](Images/A.png)

By keyframing this, we can make a fade oout animation

![fade1](Image/fade1.png) ![fade2](Image/fade2.png)

One thing to note is that the animation position of fade timeline ends up affecting the Bounce timeline. So add a keyframe in the beginning of the bounce timeline that makes it Completely Opaque.
![opaque](Images.opaque.png)
