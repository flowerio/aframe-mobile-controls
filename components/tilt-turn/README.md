# aframe-tilt-turn

Tilt your head or device to intuitively rotate [A-Frame](http://aframe.io) VR scenes. 

Have you ever been comfortably seated in Cardboard VR, and realized you would have to stand up and turn around to look at something behind you? Well, despair no more, hold your head up high, and give it a jaunty tilt to the left and right. aframe-tilt-turn has you covered.  

Mobile tools from Fasility: twoway-motion | tilt-turn

![gif](https://fasility.com/components/twoway-motion/demos/fancy-house.gif)

![Sherlock's Apartment](https://fasility.com/components/tilt-turn/demos/sherlock-holmes.gif)

![gif](https://fasility.com/components/tilt-turn/demos/sherlock-holmes.gif)

## Demos

- [Sherlock Holmes' Apartment by 3dio](https://fasility.com/components/tilt-turn/demos/sherlock-holmes.html)

Tilt a little to turn a little, tilt a lot to turn a lot.   
Tilt threshold, turn speed, and max speed are adjustable.  

## Usage 

Easy to use! Prevents the awkwardness of asking people to stand up and turn their bodies around when they are effectively blindfolded with a Cardboard headset. Works outside Cardboard mode as well, so you can easily tilt your device to look around without swiping. Together with twoway-motion, provides a super intuitive way for mobile users to get around VR scenes, with or without a VR headset.  

Make sure you are using A-Frame 0.7.0 or later. Then include aframe-tilt-turn.js in your HTML:
```html
<script src="[location of repo's dist]/tilt-turn.js"></script>
```

Then attach it to your `<a-camera>`: 
```html
<a-camera tilt-turn="criticalAngle: 20">...</a-camera>
```


## Parameters:

**Parameter** | **Default** | **Description**
------------ | ------------- | --------------
**criticalAngle** | 14 | Camera z angle (positive or negative) at which turn begins. `14` is comfortable. 
**maxTurn** | 16 | Maximum camera z angle for turning. Beyond max, tilt degree makes no difference.  
**turnScale** | 0.0025 | How fast would you like to turn? Be careful, fast spinning can make people sick! 


## Technical Details

- This component detects camera angle on the `z axis`. 
- It auto-rotates with A-Frame's built-in `look-controls`, using the `yawObject.rotation.y`.
- Has no effect on desktop or Oculus/Vive scenes. Works only on mobile devices via `AFRAME.utils.isMobile()`. 

## Credits
- Archilogic's 3dio for their incredible low-poly, high-detail models!  
- To everybody we onboarded into VR before inventing this component: We are sorry! It's super awkward to have a VR headset on your head, be blind to the world, and to try to turn your body around. 
- To couch potatoes everywhere.  
- Thanks to the A-Frame team and scene, the single best thing happening in technology today. 
