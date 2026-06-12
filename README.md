BlenderToUnity Live Sync
The Ultimate Single-File Real-Time Bridge between Blender and Unity

Version: 1.2.0 (Stable)	Render Pipelines: URP / HDRP / Built-in
Developer: Kiala Game Studio	Compatibility: Unity 2020.3+ | Blender 3.0+ & 4.0+
Dependencies: Zero External DLLs	Network Protocol: Ultra-fast TCP (No lag)
✦ Overview & Key Features
BlenderToUnity Live Sync streamlines your workflow by completely eliminating the cumbersome, repetitive task of exporting FBX/glTF files from Blender and importing them into Unity. With just a single C# file in Unity and a pristine Python add-on in Blender, you get an instant TCP live sync bridge.

Whether you are blocking out level designs, adjusting character poses, tweaking UV maps, or iterating on PBR materials, every modification in Blender is instantly reconstructed inside your active Unity scene in real time.

✔ Single File Setup ✔ Live Mesh & UV Sync ✔ Automatic PBR Conversion ✔ Edit & Play Mode Support

Zero Native DLLs: No external plugins or complex libraries. Highly secure and lightning fast.
Flawless Hierarchy & Transforms: Automatic coordinate conversion from Blender (Right-handed, Z-up) to Unity (Left-handed, Y-up).
Modern Blender 4.0+ Ready: Full support for the revamped Principled BSDF shader, correctly multiplying emission color and strength to prevent unstyled glowing white objects.
Automatic Asset Storage: Textures received from Blender are instantly saved into your Unity project directory (e.g., Assets/BlenderToUnity/Textures), automatically configuring Normal Map and Linear data profiles.
Throttled Performance: Fully customizable message queue limits prevent Unity from freezing when syncing multi-million polygon scenes.
✦ Step-by-Step Installation Guide
1
Unity Server Setup
Import the Asset package into your Unity project. If installing manually, simply copy the BlenderToUnityServer.cs script anywhere into your Assets/ folder.

Go to the top Unity menu and click:
GameObject > BlenderToUnity > Create Server

This will instantly create a GameObject named BlenderToUnityServer in your target scene, complete with a beautifully styled custom sci-fi inspector.

2
Blender Add-on Setup
Open Blender and navigate to:
Edit > Preferences... > Add-ons > Install...

Select the supplied blender_to_unity.py file and enable the checkbox next to Import-Export: BlenderToUnity.

3
Connecting the Bridge
In Blender's 3D Viewport, press the N key to open the right sidebar and click on the BlenderToUnity tab.

Make sure the IP matches your Unity machine (default is 127.0.0.1 for local sync) and Port is 9931. Click Connect to Unity.

In Unity, your inspector's LED indicator will instantly glow emerald green displaying ● BLENDER CONNECTED.

✦ Usage & Workflow
1. Manual Synchronization
In Blender's add-on panel, you have two primary one-click operators:

Sync Selected: Instantly sends all selected objects, their hierarchy, meshes, materials, and textures to Unity.
Sync Scene: Iterates through your entire Blender scene and mirrors every visible object directly into Unity.
2. Live Auto-Sync (Real-Time Editing)
Enable the Auto Sync on Edit toggle in your Blender sidebar panel. Once enabled, any action you perform in Blender—moving vertices in Edit Mode, scaling objects, applying modifiers, or editing PBR materials—will instantly update live in Unity without pressing a single button.

❖ Professional Workflow Tip
Keep Blender on your left monitor and Unity on your right monitor. You can use Unity's powerful lighting and shaders while enjoying Blender's unrivaled 3D modeling and UV unwrapping tools simultaneously!

✦ Inspector & Configuration Options
Selecting the BlenderToUnityServer GameObject in Unity provides access to several crucial operational parameters:

Parameter	Default	Description
Port	9931	The network port on which Unity listens for incoming TCP connections from Blender.
Auto Start	true	Automatically launches the TCP listening server as soon as the scene loads or Unity opens.
Flip Faces	true	Automatically reverses triangle winding orders. Highly recommended to maintain correct surface normals between Blender and Unity.
Scale Factor	1.0	Global scaling multiplier applied to all received positions and vertex arrays.
Max Messages Per Update	8	Controls how many heavy network frames (like massive meshes or 4K textures) are unpacked per Unity frame, preventing Editor freezes.
Save Textures As Assets	true	When true, decodes incoming textures into native PNG/JPG project assets so they persist permanently.
Texture Folder	Assets/...	The relative project path where synced image textures will be securely saved and imported.
✦ Frequently Asked Questions & Troubleshooting
Why are my imported objects glowing solid white in Unity?
In Blender 4.0+, the Emission Color property was updated to default to white (1, 1, 1), controlled by a separate Emission Strength slider. If you use an outdated version of the add-on, Unity interprets the white color literally. Solution: Upgrading to version 1.2.0 of this asset entirely fixes this by multiplying color and strength.

Can I connect from Blender on a remote laptop to Unity on my desktop?
Absolutely! Simply enter your desktop's local IP address (e.g., 192.168.1.50) in Blender's IP setting instead of 127.0.0.1. Ensure that your firewall allows incoming TCP traffic on port 9931.

Why do I get a CS0618 compiler warning in Unity 2023.1+?
Unity deprecated the old FindObjectOfType method. Version 1.2.0 has completely resolved this by upgrading all component searches to the modern, highly performant FindFirstObjectByType and FindAnyObjectByType methods.

❖ Connection Refused / Port in Use
If Unity reports that the port cannot be opened, another application (or an invisible background instance of Unity) might be using port 9931. Simply change the Port setting to 9932 in both Unity and Blender.

BlenderToUnity Live Sync • Developed by Kiala Game Studio • All Rights Reserved
For business support, feature requests, or custom Unity tool development, reach out via the Unity Asset Store Support Portal.
