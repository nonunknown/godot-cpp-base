# Scons for Building custom GDNative classes

**Description**
This is a modified version of sheep (godot dev) sconstruct file for use on your projects
Also it contains the base for starting with gdnative stuff

**How to use**

* Create a folder anywere or inside your godot project folder
* Place this file

**Configuration**

Those are the important lines on the file you should modify in order to get your compilation
working

#### Lines 74-77

* Local dependency paths, adapt them to your setup
godot_headers_path = "../godot-cpp/godot_headers/" # Godot headers folder
cpp_bindings_path = "../godot-cpp/" # godot cpp stuff
cpp_library = "libgodot-cpp" # the name of 

#### Lines 164-165

* Your source files (*.cpp, *.h**)
env.Append(CPPPATH=['src/'])
sources = Glob('src/*.cpp')

#### Line 65

* The path where the lib will be generated
opts.Add(PathVariable('target_path', 'The path where the lib is installed.', 'bin/'))



