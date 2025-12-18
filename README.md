Developing a Proof of Concept XR Prototype Model of a VDOT Traffic Signal Control Cabinet

https://projectfpga.com/pub/unity.html

![Alt text](CAPTURE.PNG)

Technology stack 
The proof-of-concept XR prototype for the VDOT Adaptive Traffic Controller (ATC) cabinet was developed using Unity as the primary game engine while Apple Vision Pro provides native development pathways through Xcode. Unity was chosen since it was the main language used for the course and its robust integration with Apple VisionOS via the Unity PolySpatial package. 
The implementation relied on the following major technologies and tools:
Unity 2022 LTS – Core engine for 3D modeling, asset management, physics simulation, interaction logic, and UI systems.
Unity PolySpatial + VisionOS Build Support – Enables Unity content to run inside VisionOS.
C# scripting – Primary language for interaction logic, drawer mechanics, and event-response systems.
SolidWorks – Used to create the 3D models of the cabinet frame and drawers.
Apple Vision Pro hardware – Final deployment platform for immersive XR/VR simulation.
Unity XR Interaction Toolkit (XRI) – Used to implement pick-up interactions, direct manipulation, distance grabbing, button presses, and hover detection.


Core functionality 
The final proof-of-concept prototype includes the following key capabilities:
Realistic 3D Digital Twin of the VDOT ATC Cabinet
The cabinet frame, drawers, modules, switches, and connectors are modeled with approximate dimensions and material properties to emulate the appearance of real field hardware.
Fully Interactive Components
Trainees can perform hands-on operations such as:
Opening and closing drawers
Side Panel display explaining the functionalities of each component being selected. 
Interacting with buttons, switches, and card modules


Immersive XR Training on Apple Vision Pro
The prototype deploys directly to Vision Pro, allowing trainees to:
Walk around the cabinet in 3D space
View the internal layout with natural head movement and spatial depth
Use hand-tracking to interact with components
Perform procedures without risk to equipment or safety
Collectively, these features create a functional training environment where new technicians can safely practice handling a complex traffic controller cabinet before working on physical hardware.


Key technical decisions 
Several design choices guided development:
Imported vs built assets
While the use of already designed assets speeds up the modellng, we couldnt get all assets . we took the decision to build from scratch in unity most of the assets up to 80 percent of the assets were built in unity and solidworks. .


Direct Manipulation Interaction Model
Instead of abstract UI menus or laser pointers, we implemented natural hand-based interactions enabled by Vision Pro’s hand-tracking. This improves training realism and reduces user onboarding time.


Modular Cabinet Architecture
Each drawer, cable, and component is implemented as a modular Unity prefab with its own interaction script. This makes the system more extensible for future additions such as:
Multiple cabinet types
Different ATC versions


Physics-Based Movement for Components
Rather than simple animations, drawer motions and cable interactions use Unity physics to achieve more realistic behavior and allow for unplanned user actions (e.g., partially opened drawers or cables dropped on the floor).






4. Dependencies/constraints 
The prototype assumes:
Approximate dimensional references for the cabinet and its components, we couldn't get an exact prototype of the hardware so we designed it from scratch in solidworks and unity. 
Vision Pro hardware availability for deployment and testing.
Apple VisionOS Unity supports limitations, such as specific shaders, physics, or UI elements that are not fully compatible with PolySpatial.
Not all real ATC electrical functions are simulated—the proof-of-concept focuses on physical interaction, and  basic signal logic. Interactions like signal output or led outputs were not modelled.
Limited training scope due to time and resource constraints; only selected operations are included in the prototype.


2. System Architecture (0.5–1 page)
The VR / AR headset that was used for this project is the Apple Vision Pro.  As such, the system architecture was set up to interface with the Vision Pro.  While Apple has its own game engines such as Xcode and RealityKit, this project was developed using the Unity game engine instead, primarily because of the wider range of deployment options.  The consequence of using Unity is that several changes were made to the Project that allowed for the addition of the correct components and scripts.  The diagram below shows the system architecture with a primary emphasis on the Unity packages, components, and build profile options that were used.


