
# Inscryption port for PS VITA

This repos contains patch you can apply on Inscryption Steam data files in order to get the game running on PS VITA.

**Please read carefully following sections before going on with the patching procedure**

## Notes

Inscryption is a quite recent game that relies a lot on graphics (arts, effects, lighting, …) for its ambiance, so porting it on our old beloved vita required some sacrifices. 

Don’t expect the same graphics and performance as official versions, but I personally find the ambiance and game feel remains intact. 

Considering the type of game, I tried to reach a frame rate around 15 fps, which was for me the right balance between comfort, graphics quality and cpu/ram usage. See for yourself the result in the video below.

Here is a video showcasing the first 14 minutes of gameplay (don’t bother the video quality & misplay's, goal is to see how the game runs and is played) :

[![Showcase video](https://img.youtube.com/vi/xkCgldud1hA/0.jpg)](https://www.youtube.com/watch?v=xkCgldud1hA)

If not yet done, support the dev by buying the game.

## Sacrifices had to be made

- All shaders had to be rewritten for vita specs, so expect visual differences
- Textures resolution decreased
- Meshes (3D models) have been simplified for cpu and ram usage
- Some meshes were removed or replaced (for critical ones) because they were broken
- Some tricks were used to reach a decent frame rate (reduced field of view, shortened animations, hidden objects)
- Some languages were removed for ram usage : Chinese, Japanese, Russian, Turkish (sorry guys)

## Controls

Cursor can be moved with touch screen but is (most of the time) not clickable.

Some parts can be played using dpad (card selection, table slot selection, map destination selection, …)
- X/L : select (where cursor is or on highlighted interactable)
- R : Ring bell to end turn
- Dpad : Change interactable selection / Move player
- Right stick : Look / Flip rulebook page
- Triangle : Open rulebook when cursor is on rulebook icon
- Circle : Cancel
- Start : Open Pause menu

## Known issues (that could be addressed in future version if any)

- Rulebook in cabin is buggy (low perf shader + page changing to right )
- Subtitles are not visible when playing videos
- Framerate drops when some animations are running
- Some meshes are missing
- Teeth collisions are sometimes buggy
- Crash can happen when vita is running out of memory (as usual with Unity games)
  
## PS VITA Set up

In order to have the best possible experience, I recommend you to use following plugins (that you should be able to find somewhere on the net) :
- ioplus.skprx
- iostaging.skprx

**+ Full CPU Overclock (500Mhz)**

## Patching procedure

- Download Inscryption vpk from vitadb or from latest release and install it.
- Go to the Release page and download ``InscryptionVitaSteam.zip``.
- Extract it.
- Put the game's data folder(```../steamapps/common/Inscryption/Inscryption_Data```) inside the extracted folder (Should be official Steam version 1.10)
- Launch ``ApplyPatch.bat`` and wait.
- Let it finish and there should be a .ZIP file named ``InscryptionVita.zip``.
- Open VitaShell, connect your PS Vita to your PC and copy the contents of the .ZIP file```(Zip file should be around 650MB before unpacking)``` over to ``ux0:app/INSC12345/``.
- Click on "Replace the files in destination" when it asks you to.
- Launch the game and have fun!
