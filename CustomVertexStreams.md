---
layout: default
title: Custom Vertex Streams
nav_order: 5
---

## Custom Vertex Streams

Many Particle Effects parameters are controlled via Custom Vertex Streams. Such parameters like Emission Power, Dissolve Progress, Appear and Disappear, Random Offset for Noise Textures, and etc. Check the name of a shader used in the Particle System, find it on this page, and check what each Custom Vertex Stream does. Try to modify, for example, the Dissolve Progress parameter for the "DissolveParticleAdvanced" shader and make particles disappear quicker or slower.

![s17](/assets/images/Screenshot_17.png)

For more information, you can check the official Unity Documentation: [https://docs.unity3d.com/Manual/PartSysVertexStreams.html](https://docs.unity3d.com/Manual/PartSysVertexStreams.html)

### DissolveParticleSimple:

* **Custom1.X / UV0.Z** - Random value for adjusting the offset of Main Texture
* **Custom1.Y / UV0.W** - Random value for adjusting scale of the Main Texture
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Random value for flipbook frames

### DissolveParticleAdvanced:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affecting opacity
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams

### DissolveParticleDepth:

* **Custom1.X / UV0.Z** - Emission Multiplier, control the emission power over the lifetime
* **Custom1.Y / UV0.W** - Offset and Dissolve Progress, this parameter will affect both the dissolve and offset parameters
* **Size / UV1.X** - Adjusting the scale multiplier depending on particle size (No need to modify this parameter, it is a fix)

### DissolveParticleGroundPacked:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Secondary Mask (Appear/Initialize) progress, use this to make effect appear
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Lava Appear progress, control the appearence of lava

### FakeTrailAndMeshFireParticles:

* **Custom1.X / UV0.Z** - Control the U gradient mask, used for fade in and fade out effects of the fire
* **Custom1.Y / UV0.W** - Custom UV offset animation, moving the whole fire mask texture, used to make moving fire trail look more realistic
* **Custom1.Z / UV1.X** - Random value for each particle, to make them look slightly different

### DissolveParticleMV / DissolveParticleFlipBook:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Distortion Power Multiplier, used to control texture distortion over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Emission Multiplier, control the emission power over lifetime
* **Custom2.X / UV1.Z** - Secondary Mask offset, used to multiply opacity by moving this mask texture with Vertex Streams
* **Custom2.Y / UV1.W** - Secondary Mask negate, use this to control how much Second Mask affecting opacity
* **Custom2.Z / UV2.X** - Distortion Mask offset, used to multiply distortion by moving this mask texture with Vertex Streams
* **Custom2.W / UV2.Y** - Custom frame animation control for a flipbook texture, enable "MV Particle Frame Control Enabled" parameter in material settings to use this Vertex Stream.

### CenterCurve:

* **Custom1.X / UV0.Z** - Random value for each particle, to make them look slightly different
* **Custom1.Y / UV0.W** - Emission Multiplier, control the emission power over lifetime
* **Custom1.Z / UV1.X** - Dissolve progress, used to control the dissolve effect
* **Custom1.W / UV1.Y** - Second Mask offset progress, used to move the second mask on V coordinate

### Props:

* **Custom1.Z / UV1.X** - Dissolve/Appear Effect progress control. Used to control the dissolve effect of the mesh when it appears or disappears.



### Support email: sinevfx@gmail.com
