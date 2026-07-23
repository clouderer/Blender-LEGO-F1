# LEGO F1 car
F1 car in the lego style modeled in blender.
This was my very first project in blender - this project took about 50 hours (trial and error time included). 

https://github.com/user-attachments/assets/722df4d2-70e2-4ea6-ab4f-c22e720087c4

## Development Process

<details>

### Modeling Process

The model was built using reference images obtained from a previous vectorization task, providing accurate front and side views of the Formula car.

### Wheel Construction

The car was constructed in individual components, starting with the wheels:

> **Tip:** If you want to replicate this workflow, I strongly recommend modeling the components from the inside out rather than from the outside in.

Since all four wheels are identical, I only modeled a single wheel and used modifiers (**Array** and **Mirror**) to place the rest. 

<img width="873" height="729" alt="image-1" src="https://github.com/user-attachments/assets/d1a9dc5b-d15a-4c14-9146-85e5f23815c0" />

**Techniques used for the wheel:**
* Started with a base **Cylinder** primitive.
* Added **Loop Cuts** to define the tire tread grooves.
* Used **Extrude** and **Inset** tools to shape the rim geometry.

### Engine & Frame Construction

Next, I worked on the Formula car's engine assembly using the same core modeling techniques. To manage the complexity, I broken the engine down into several smaller sub-components (such as the flag pole, the flag itself, and the pole mount). 

To streamline the workflow, I modeled only one half of the engine structure and applied a **Mirror Modifier** across the symmetry axis.

#### Modeling LEGO Studs
Unlike the wheels, several engine components featured functional LEGO studs. These were built directly into the geometry of individual blocks using the following technique:
1. Placed **Loop Cuts** on the block surface to isolate a square face.
2. Subdivided the square face and applied a **Bevel** to the central vertex to form a round profile.
3. Used **Extrude** to raise the stud from the surface.

#### Flag Mount Detail
The flag mount was created starting from a standard **Cylinder** primitive:
* Inset the top face to establish the inner wall boundary.
* Deleted redundant vertices, edges, and faces, then manually bridged the remaining geometry to achieve the base shape.
* Used a **Boolean Modifier** to join a cube primitive with the modified cylinder, completing the mount's final structure.

<img width="1398" height="1061" alt="image-3" src="https://github.com/user-attachments/assets/2a2fdf54-e228-45cf-9cba-894e05b83427" />
<img width="1013" height="674" alt="image-2" src="https://github.com/user-attachments/assets/4b920bd9-0801-4b56-ac11-241f3f9d2a88" />

### Base Chassis, Bodywork & Suspension

Following the completion of the engine, I constructed the base chassis to serve as the structural foundation for the rest of the build. 

The chassis was created from a halved **Cube** primitive, shaped using a combination of **Extrude**, **Loop Cut**, and **Scale** operations alongside targeted vertex manipulations. As with previous components, a **Mirror Modifier** was applied to maintain symmetry efficiently.

<img width="1065" height="417" alt="image" src="https://github.com/user-attachments/assets/021904eb-7f13-476a-8b71-4ff9cda34670" />

#### Bodywork & Front Wing
Using the same core techniques established during the engine and chassis construction, I modeled the outer bodywork and the front wing assembly. 

<img width="1221" height="531" alt="image" src="https://github.com/user-attachments/assets/ec0e3e62-989e-4e59-82bb-57fc33e4b342" />


#### Wheel Mounting Points
The suspension and wheel mounting components were constructed using a workflow similar to the one used for the wheels, ensuring geometric consistency across the entire assembly.

<img width="1301" height="1155" alt="image" src="https://github.com/user-attachments/assets/f3f42ea5-a897-48c8-b8bc-6310b3b202de" />


### Rear Wing Assembly

Modeling the rear wing assembly required a more intricate workflow, particularly due to the curved mounting block supporting the wing structure.

* **Mounting Block:** I achieved the rounded contours of the support block using the **Bevel** tool, then cleaned up and refined the resulting geometry topology using the **Knife** tool.
* **Side Wing Panels:** The side panels proved to be the most complex parts of the build. Because I initially tapered the base **Cube** primitive, detailing it required precise adjustments using **Loop Cut**, **Knife**, and **Bevel** (applied specifically to smooth the inner edge transitions).
* **Main Wing Element:** In contrast, the central wing section spanning between the panels was more straightforward:
  1. Applied **Extrude** to the side face of a cube.
  2. Shifted and angled the extruded geometry to form the main wing profile.
  3. Applied **Bevel** to the outer corners to round off the edges.
 
  <img width="1306" height="1014" alt="image" src="https://github.com/user-attachments/assets/289f3aff-1aec-49ca-a18b-3d46f57a722d" />

  ### Finalizing the Bodywork & Wheel Suspension

Modeling the remaining sections of the bodywork was straightforward, relying on the repeated application of the techniques detailed above (as shown in the final image of the Modeling section).

#### Suspension & Hub Assembly
The wheel suspension units were created starting from an **UV Sphere** primitive:
1. Selected and extruded the polar cap geometry to form the core attachment joints.
2. Joined a **Cylinder** primitive to complete the suspension strut structure.

<img width="788" height="769" alt="image" src="https://github.com/user-attachments/assets/136cf518-a644-464f-b90d-6fedebfc06a2" />

#### Steering Wheel
The steering wheel was built using **Cube** primitives as the base mesh and shaped using a combination of **Bevel**, **Extrude**, and **Loop Cut** operations to achieve the final ergonomic design.

<img width="797" height="594" alt="image" src="https://github.com/user-attachments/assets/1fdb6006-8711-4163-a6eb-0ab339a23de6" />

#### Halo Safety Structure
The Halo guard was constructed using a **Bézier Curve** as the main path guide, with its cross-sectional profile defined by a **Bézier Circle** object (using the curve's Bevel Object settings).

<img width="1463" height="589" alt="image" src="https://github.com/user-attachments/assets/cc6945ed-ec95-4fa8-be78-3d3fac63264a" />


### Materials & Texturing

Since this model represents a LEGO car with a clean, straightforward color palette, I created a set of base materials with specific color, roughness, and specular settings, which were then applied across the various components.

<img width="1191" height="479" alt="image" src="https://github.com/user-attachments/assets/42925928-805e-4e0c-925e-c6f4550cdeef" />


#### Decals & Logos
Certain elements (such as the rear wing) feature sponsor logos. To incorporate these:
1. Source/created transparent **PNG** decal textures.
2. Mapped the images onto the corresponding object geometry using **UV Editing** and custom UV layouts.
