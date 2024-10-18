# 3D Modelling

3D modelling is generally the process of creating digital representations of surfaces in three dimensional spaces. For the purposes of game development, this will be either through poly modelling or sculpting.
A common workflow in game development might look something like Modeling -> UV Mapping -> Texturing -> Baking -> Rigging -> Animation -> Export, but many steps like baking and rigging may not be necessary depending on the model's purpose.
It is important to note that many programs disagree on how to handle 3D space or express textures.

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
### Blender Sculpting
  Blender supports sculpting competently for a generalist, free 3D software. It misses some optimizations available to dedicated sculpting packages. Many tutorials produced in Blender 2.8 will reference tools that may have moved in the UI, but can often be located by name through search, the default hotkey to search by name is F3.
-[Grant Abbitt Learn Sculpting in Blender Series](https://www.youtube.com/playlist?list=PLn3ukorJv4vvJM7tvjet4PP-LVjJx13oB)
-[Flipped Normals Sculpting Quickstart](https://www.youtube.com/watch?v=Cmi0KoFtc-4)
-[Yan Sculpts Sculpting in Blender Series](https://www.youtube.com/playlist?list=PLvPwLecDlWRCXSVh0nskG810BAerdz9DW)
-[Ryan King Art Retopology Introduction](https://www.youtube.com/watch?v=1myOZaxtHes)
-[Grant Abbitt Baking](https://www.youtube.com/watch?v=MUTdHgif65g)
### ZBrush
### Mudbox 
## Texturing
### Substance Painter
### 3DCoat
### Blender Texturing
## Common Pitfalls
### Left and right handed
### Baking green channel 
### Y up Z Up
