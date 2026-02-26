A new class/Control node for Godot that acts as an object you can Drag & Drop, with juicy effects built in.

Features pick up effects, damped oscillator velocity on drag, shader-based faux-3D-rotation on hover, shadows, etc...

**Instructions:** 
- Apply the script to any Control node to make it draggable, or (smarter) extend the Draggable class with new functionality for your use-case.
- Set the `drop_area` in the inspector to any Control node that, when the Draggable is dropped on it, will emit the `drag_successful` signal from the Draggable. Use this signal to determine what happens.
- Optionally, assign a node to act as the `face` and `bounds_override` of the Draggable.
  - `bounds_override` determines what acts as the "clickable" surface of the Control. What can you grab hold of to drag it? If unset, uses the bounds of the object the script is on.
  - `face` handles the visual side of things, determinging what gets affected by the fake 3D rotation. Should be a `TextureRect`. Without this, we still get most of the basic dragging functionality, just not 3D rotation through a shader.

**TODO:**
- Handle inputs other than mouse
- Update documentation
- Add examples
- Implement a more intuitive version of the `face`. Can it be something other than `TextureRect`?

Originally based on the Balatro cards recreation by MrEliptik: https://www.youtube.com/watch?v=Alwy-TH0WzE&pp=ygUbYmFsYXRybyBjYXJkcyBnb2RvdCBlZmZlY3Rz
