BlenderToUnity 

Real-Time Scene Sync (Free)

BlenderToUnity is a lightweight real-time bridge between Blender (3.0+) and Unity.
It allows you to sync your entire Blender scene directly into Unity with live updates — including transforms, meshes, materials, textures, hierarchy, and animation playback.
No manual exporting. No FBX re-importing. Just press Connect and start working.
________________________________________
🚀 Features

✅ Real-time transform sync (position, rotation, scale)

✅ Live mesh reconstruction (Edit Mode, Sculpt, Modifiers)

✅ Material color sync (Principled BSDF – Base Color)

✅ Texture transfer (Image Texture → Unity material)

✅ Automatic texture repaint updates (Texture Paint)

✅ Hierarchy synchronization (parent/child relationships)

✅ Object deletion handling

✅ Animation playback sync (frame-by-frame mesh deformation)

✅ Visibility sync (hidden objects disabled in Unity)

✅ One-click server creation inside Unity

________________________________________
🔧 How It Works

Blender sends scene data over a local connection (default port 9931) to Unity, where a lightweight server component reconstructs and updates GameObjects in real time under a root object called: BlenderSync
All changes in Blender are reflected immediately in Unity.
________________________________________
📦 Installation

Unity Side

Copy
unity/Assets/BlenderToUnity/BlenderToUnityServer.cs
into your project's Assets/ folder.
In Unity, go to:
GameObject > BlenderToUnity > Create Server
(or manually add the BlenderToUnityServer component to an empty GameObject).
The server starts automatically on port 9931 (autoStart enabled by default).
Check server status in the Inspector.
________________________________________
Blender Side (3.0+)

Go to Edit > Preferences > Add-ons > Install...
Select:
blender_addon/blender_to_unity.py
Enable the addon "BlenderToUnity"
In the 3D View, press N to open the sidebar
Open the BlenderToUnity tab
Click Connect
(Default: 127.0.0.1, Port 9931)
✅ The entire scene is immediately transmitted to Unity.

________________________________________
🔄 Live Sync Behavior

Action in Blender	Result in Unity

Move / Rotate / Scale object	Transform updates in real time
Edit mesh (Edit Mode, Sculpt, Modifiers)	Mesh rebuilt dynamically
Change material color (Principled BSDF)	Material color updated
Add Image Texture to Base Color	Texture sent and applied
Paint texture (Texture Paint)	Texture auto-resends
Change parent hierarchy	Hierarchy replicated under BlenderSync
Delete object	GameObject removed
Play animation (▶ timeline)	Mesh deforms frame-by-frame
Hide object	GameObject disabled
________________________________________
🎯 Ideal For

Rapid prototyping
Level blockout workflows
Environment design iteration
Technical artists
Blender-focused pipelines
Indie developers wanting faster iteration cycles
________________________________________
⚠️ Notes

Designed for local workflow (localhost connection).
Works best during development — not intended for runtime builds.
Optimized for iteration speed rather than production export replacement.
________________________________________
❤️ Free & Open Tool

This asset is completely free to help speed up your workflow and support the Blender + Unity community.
If you find it useful, consider leaving a review — it helps a lot!
________________________________________
Se quiseres, agora posso:

✅ Criar uma versão mais curta e mais "marketing-driven" (a Asset Store gosta de textos mais diretos)
✅ Escrever a Short Description (até 200 caracteres) que aparece no topo
✅ Preparar o texto para a secção Technical Details
✅ Fazer uma checklist final para garantir que passa na revisão da Unity sem rejeição

