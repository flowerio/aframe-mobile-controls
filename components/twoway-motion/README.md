# aframe-twoway-motion 

Touch movement controls for [A-Frame](http://aframe.io) VR scenes on mobile devices.  
Move forward and backward in an A-Frame environment on your phone.  
Supports Portrait, Landscape and Cardboard modes.  

Mobile tools from Fasility: twoway-motion | tilt-turn

![gif](https://fasility.com/components/twoway-motion/demos/twoway-motion-3.gif)

## Demos

- [Fancy House by 3Dio](https://fasility.com/components/twoway-motion/demos/fancy-house.html)
- [4 murals by Howie Green](https://fasility.com/howie)

Tap to move forward. To move backward, look downward, then tap.  
Movement speed and downward threshold are adjustable.  

## Usage 

Make sure you are using A-Frame 0.7.0 or later. Then include aframe-twoway-motion.js in your HTML:
```html
<script src="[location of repo's dist]/twoway-motion.js"></script>
```

Then attach it to your `<a-camera>`: 
```html
<a-camera twoway-motion="speed: 35">...</a-camera>
```


## Parameters:

**Parameter** | **Default** | **Description**
------------ | ------------- | --------------
**speed** | 40 | Motion speed. `40` is a brisk walking pace. 
**threshold** | -40 | The x angle at which the cursor will turn orange and motion will be backward. `-10` would be just below the horizon.
**nonMobileLoad** | false | twoway-motion will not run unless it is on a mobile device. Set nonMobileLoad to `true` to load it anyway. 


## Technical Details

- This is a lightweight alternative to `Universal Controls`. Does not require physics. 
- Plugs directly into A-Frame's native `wasd-controls`.
- Has no effect on desktop or Oculus/Vive scenes. Works only on mobile devices via AFRAME.utils.isMobile(). 
- Ignores multitouch (Touch events with more than one touch point). 
- Does not preventDefault on the Touch event. You can still click things with the cursor. 
- twoway-motion is not for 360 pictures. It will only distort the 360 panorama in interesting ways. twoway-motion is for exploring 360 scenes on mobile in handheld and cardboard modes. 

## Credits
- Archilogic's 3dio for their absolutely amazing models!  
- Initial idea made for Howie Green's HowieSpace so that people could have a better experience of an artistic mural than pinching and zooming a photo on a mobile phone. 
- Thanks to Don McCurdy for starting the party with A-Frame Extras' `Universal Controls`! 
- Greets to the A-Frame team, contributors, component authors and everybody in the scene!
