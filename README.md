# Scons for Building custom GDNative classes

**News**
* Updated to support NativeIntegration plugin:
  - added `src_folder` arg eg: `src_folder = "src/project_name/"`
  - ps: using with `target_path` arg eg: `target_path = "bin/project_name/"`

**Description**

This is a modified version of sheep (godot dev) sconstruct file for use on your projects
Also it contains the base for starting with gdnative stuff

**How to use**

* Clone this repo inside any folder or inside your godot project
* Then clone the godot-cpp repo inside this folder

**Configuration**

There's no need to change anything, only if you like to, just make sure to place
your cpp and hpp files inside `src/` folder

**Example Commands**

`scons platform=linux target=release -j4 `

`scons platform=windows target=debug -j3 src_folder="src/windows_stuff target_path="bin/windows_stuff"`
