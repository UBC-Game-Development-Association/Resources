# 3D Modelling

3D modelling is generally the process of creating digital representations of surfaces in three dimensional spaces. For the purposes of game development, this will be either through poly modelling or sculpting.
A common workflow in game development might look something like Modeling -> UV Mapping -> Texturing -> Baking -> Rigging -> Animation -> Export, but many steps like baking and rigging may not be necessary depending on the model's purpose.
It is important to note that many programs disagree on how to handle 3D space or express textures.

*This document is currently trying to provide an introduction to each discipline and software referenced.*

## Poly Modeling
### Blender 
Blender is a free and open source 3D Modelling suite with a large online community. Tutorials from before Blender 2.8 will be very hard to follow, 2.8 and onward will generally be quite similar.
- [Grant Abbitt Welcome to Blender 4.0](https://www.youtube.com/watch?v=lLqep5Q4MiI)
- [Grant Abbitt Low Poly Modelling Series](https://www.youtube.com/playlist?list=PLn3ukorJv4vsPy9J9x4--pat6jaPqNm11)
- [Blender Guru Donut Tutorial 4.0](https://www.youtube.com/playlist?list=PLjEaoINr3zgEPv5y--4MKpciLaoQYZB1Z)
  - This is a very traditional Blender tutorial. It can be somewhat controversial, but is a very good survey of many of Blender's tools, not all of which are going to be used in GameDev tasks.
- [Pixxo 3D Modelling A Simple Human](https://www.youtube.com/watch?v=9xAumJRKV6A)
### Maya
Maya is Autodesk's industry standard 3D Poly Modelling software. A student license can be acquired for free, for learning and non-commercial use by sending Autodesk evidence of enrollment.
- [Maya Learning Channel Maya 101](https://www.youtube.com/playlist?list=PLD8E5717592CF5C26)
- [Flipped Normals 1 Hour Maya Quickstart Guide](https://www.youtube.com/watch?v=kYQ98Q5UmNo)
### 3DS Max
Maya is Autodesk's other industry standard 3D Poly Modelling software. A student license can be acquired for free, for learning and non-commercial use by sending Autodesk evidence of enrollment. 
- [3DS Max Learn to 3D Model Anything](https://www.youtube.com/watch?v=q2QGaKCyCBM)
- [3DS Max Beginner Tutorial 2024](https://www.youtube.com/watch?v=gVTkLG5EaLE)
## Sculpting
Sculpting is a technique that is often used with poly modeling to add detail. Using extremely dense meshes, high levels of detail are painted onto models. This can be a very effective way to create detailed models, but often the dense models are not viable for use in games. This requires **retopology**, the creation of a low polygon approximation of the high poly model, and **baking**, creation of a detail map to transfer the detail from the high poly model to the low poly model.
### Blender
  Blender supports sculpting competently for a generalist, free 3D software. It misses some optimizations available to dedicated sculpting packages. Many tutorials produced in Blender 2.8 will reference tools that may have moved in the UI, but can often be located by name through search, the default hotkey to search by name is F3.
- [Grant Abbitt Learn Sculpting in Blender Series](https://www.youtube.com/playlist?list=PLn3ukorJv4vvJM7tvjet4PP-LVjJx13oB)
- [Flipped Normals Sculpting Quickstart](https://www.youtube.com/watch?v=Cmi0KoFtc-4)
- [Yan Sculpts Sculpting in Blender Series](https://www.youtube.com/playlist?list=PLvPwLecDlWRCXSVh0nskG810BAerdz9DW)
- [Ryan King Art Retopology Introduction](https://www.youtube.com/watch?v=1myOZaxtHes)
- [Grant Abbitt Baking](https://www.youtube.com/watch?v=MUTdHgif65g)
### ZBrush
* ZBrush is an industry standard sculpting software that is extremely well optimized for sculpting. It is incredibly unintuitive and has a steep learning curve, but is very powerful. It is quite expensive. Maxon offers a reduced annual subscription for students.
- [Pixologic Tutorials](https://zclassroom.com/zclassroom/workshop/getting-started-with-maxon-zbrush)
- [Al Howell Learn ZBrush in 2024 Series](https://www.youtube.com/playlist?list=PLPczLadouqi-wLOizlZHAOLbfEas5Xc0L)
- [Pixologic Youtube Channel](https://www.youtube.com/@MaxonZBrush)
    - The company that produces ZBrush, Pixologic, has a near constant stream of professional artists using ZBrush on their youtube channel.
## Texturing
Texturing is broadly the process of describing how a 3D model is rendered. Nearly every 3D software tool will have different systems for this process. Broadly, a **material** is created as a collection of properties that describe the behavior of light hitting the model. One of the most efficient techniques and transferrable techniques is **baking** procedural designs or layers of painted textures to a single image for each property of the material that is being used, because it will be applied similarly in each tool. For every thorough description of modern rendering and materials [the PBR Book](https://pbr-book.org/)
### Blender
- [Grant Abbitt Texture Painting Tutorials](https://www.youtube.com/playlist?list=PLn3ukorJv4vtvjZvdiOeoSA5kBohtnDOF)
- [Grant Abbitt Baking](https://www.youtube.com/watch?v=MUTdHgif65g)
- [Brandon3D Introduction to Material Shading In Blender](https://www.youtube.com/watch?v=Wg244y2f9Fw&t=35s)
- [CrossMind Studio Shading/Texturing/UV Tutorial](https://www.youtube.com/watch?v=qsXlL1WXEQA)
### Substance Painter
Substance Painter is a professional grade 3D texturing software, which reflects many similar industry tools like Mari. It was bought by Adobe, and may be part of the Adobe Student license. Perpetual licenses with one year of updates are available through Steam. It is a layer based 3D painting system, that can be used to 
- [Algorithmic Getting Started With Substance Painter Series](https://www.y+outube.com/playlist?list=PLB0wXHrWAmCwnqWfKdGEmbtSKN2EzvLrY)
- [Michael Tanzillo Adobe Substance Painter Training](https://www.youtube.com/playlist?list=PLfAG6wq8HC-9CP7VoTHwGvGWJtcScHLYP)
- [JL Mussi Learn Substance Painter in 80 Minutes](https://www.youtube.com/watch?v=s2MOx1Iteik)
### 3DCoat
3DCoat, produced by Pilgway, is another suite with baking, texturing and sculpting abilities. It has educational licenses and perpetual licenses. The texturing is another layer based 3D Paint tool like Substance Painter.
- [Pilgway tutorials](https://3dcoat.com/tutorials/)
- [Nexttut 3DCoat Handpainted Textures Tutorial](https://www.youtube.com/watch?v=ld4qBMBL0fg&t=365s)
## Common Pitfalls
### Differences between softwares
- Different 3D softwares will define certain aspects of 3D space differently. Partly due to rendering backends, as well as due to debates about how to project three dimensions into the two dimensional space of the screen, there are two key dimensional differences. ***Left-handed vs Right-handed*** and ***Y-Up vs Z-Up*** are the primary ways of sorting 3D programs. Left and right handedness describes the direction of the axis of depth, the one that goes into or out of the screen, often X by default. In a left handed coordinate system, that axis increases in the positive direction as it goes away from the viewer and into the screen, while a right handed system will increase positively going toward the viewer, coming out of the screen. Similarly, systems do not agree as to whether the Y or Z axis should be the one that points up on the screen by default. Y up might be imagined as drawing an X-Y plane on a piece of paper laying flat, then rotating it so that it now stands and faces you as if pressed against your monitor, and the missing axis, that of depth would then be Z. Z Up might be imagined as taking that flat paper with X-Y plane, and adding the third dimension, height, and naming that as your Z axis. There are arguments for each system, but if you export a 3D model from one software to another, and it is unexpectedly rotated, these differences in coordinate system are likely culprits, and can often be solved in export settings.
![image](https://github.com/user-attachments/assets/bde6a227-5641-469c-a071-3bbf9b9f90c7)
- If baking a normal map, there are many different formats that can be used in calculation. Most commonly three channels of an image, Red, Green, and Blue, are used to encode information about the X, Y, and Z axes accordingly. If a baked map from one program does not look correct in another, a common culprit is that the other program is using an ***inverted green channel***. Using a filter in a photo editing software is a quick fix. Maya is the most common software that uses an inverted green channel in bakes, but it is common in Game Engines as well, because of the different backends used. Blender and many open source tools will often default to the **OpenGL** system while game engines like Unreal Engine will often use the **DirectX** system.
