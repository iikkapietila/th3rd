"th3rd"
Realtime demo released at Instanssi 2023 event in Instanssi-demo series. 2nd place.

th3rd_by_nisual_plive.exe is a single file independent executable for running the demo.
th3rd_by_nisual_plive_source.zip is a zip file containing the original source code and resources (.glsl-files, music, and font).

Zip file is organized in the following manner:
main.py -python file
programs -folder
moderngl_window -folder

Glsl-files are found in both folders, this is because I held different versions for development and .exe bundling. You can use this project as a basis for your own experiments, for instance intro or demo project. Just replace the glsl-files with your own shaders and include your own music. Bundle the project into a single executable with e.g. pyinstaller.

Make sure to define paths correctly on lines 41-43:

#os.chdir(sys._MEIPASS) <--- this is needed when bundling to exe as this refers to the temp folder in which the resources are found

#use_path = 'moderngl_window\\scene\\programs\\' <--- alternative folder for using different resource files for bundling the exe

#use_path = 'programs' # When running this from Python ide, define the resources folder here, i.e. path to .glsl files

On lines 147-154 there's a label for displaying runtime, number of the loaded shader and amplitude of the audiotrack. This may help you in debugging.
