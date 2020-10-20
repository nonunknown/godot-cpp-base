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

Those are the important lines on the file you CAN modify, but its not mandatory
#### Lines 74-77

* Local dependency paths, adapt them to your setup:
```
godot_headers_path = "../godot-cpp/godot_headers/" # Godot headers folder
cpp_bindings_path = "../godot-cpp/" # godot cpp stuff
cpp_library = "libgodot-cpp" # the name of 
```
#### Lines 164-165

* Your source files (*.cpp, *.h**):
```
env.Append(CPPPATH=['src/'])
sources = Glob('src/*.cpp')
```
#### Line 65

* The path where the lib will be generated:
```
opts.Add(PathVariable('target_path', 'The path where the lib is installed.', 'bin/'))

```

