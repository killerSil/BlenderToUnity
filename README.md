Installation

Unity Side
1. Copy `unity/Assets/BlenderToUnity/BlenderToUnityServer.cs` to the `Assets/` folder of your project.

2. Menu **GameObject > BlenderToUnity > Create Server** (or add the `BlenderToUnityServer` component to an empty GameObject).

3. The server starts automatically on port **9931** (`autoStart`). Check the status in the Inspector.

Blender Side (3.0+)
1. **Edit > Preferences > Add-ons > Install...** and choose `blender_addon/blender_to_unity.py`.

2. Activate the "BlenderToUnity" addon.

3. In 3D View, press **N** to open the sidebar → **BlenderToUnity** tab.

4. Click **Connect** (host `127.0.0.1`, port `9931`). The entire scene is sent immediately.

---

How it works

| Action in Blender | Result in Unity |

|---|---|

| Move/rotate/scale object | Transform updated in real time |

| Edit mesh (Edit Mode, sculpt, modifiers) | Mesh rebuilt |

| Change material color (Principled BSDF) | Material color updated |

| Texture in Base Color (Image Texture) | Texture sent and applied in Unity |

| Paint the texture (Texture Paint) | Texture automatically resent |

| Change hierarchy (parent) | Hierarchy replicated under `BlenderSync` |

| Delete object | GameObject removed |

| Play animation (▶ on timeline) | Meshes deformed frame by frame in Unity |

| Hide object | GameObject disabled |
