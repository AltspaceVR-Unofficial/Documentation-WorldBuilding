# Configuring Your World For Display On The Oculus Quest & Go
**(And other Oculus mobile platforms)**
****
## Intro
Currently, for display on Oculus mobile platforms, AltSpaceVR requires some light configuration within a template's `Project Settings`. Previously, this was handled automatically by the `Unity Uploader`. _However_, **as of Uploader version 0.8.7**, _this is not longer configured automatically_. This documentation reflects the current steps required to get custom worlds to display on Oculus-powered mobile devices.

## How-To
1. Open `Project Settings` from the `Edit` menu.
2. Navigate to `Player Settings` and select the `Android` icon ([represeneted by a trash-bin shaped robot](https://commons.wikimedia.org/wiki/File:Android_robot.svg))
3. Scroll down to `XR Settings` and check `Virtual Reality Supported`.<sup>a</sup>
4. In the list of `Virtual Reality SDKs`, click the `+` button and select `Oculus`.
5. Scroll down to `Stereo Rendering Mode` and set it to `Single Pass`.
6. That's it! When ready, build your world with `Android` support _checked_ in the Unity Uploader.

<sup>a</sup> **Important Note:** _Do **NOT** use the "new Unity XR Plugin System" nor the `XR Plugin Management` section, as this will **at best** break compatibility with PC VR, and **at worst, prevent your world from building at all!**_
****
### Q. I already installed the `XR Plugin System`; Now what?!
#### A. _Don't Panic_. Just follow these steps and you'll be "right as rain":
1. Open `Package Manager` from the `Window` menu.
2. Search for `XR` in the package search box.
3. For each item _starting with `XR`, or containing `XR` **in the name**,_ click it, and select `Remove` from the bottom right.
4. Once _all relevant packages are removed_, follow the instructions from [How-To](#how-to) as normal.

### Q. That didn't fix it!
#### A. In the event that the `XR Plugin System` has already borked your project beyond repair, follow these steps.
1. In the **Asset Browser**, navigate to `Scenes` and locate the scene used as your world template.<sup>b</sup>
2. Right-click the scene file and select `Export Package`.
3. Follow the steps to save a unity package and wait for the export to complete.
4. Close the Unity project.
5. Locate the folder for your unity project and add `_old` to the folder name.
6. Create a new Unity `2019.4.2f1` project and name it the same name as your original project's name.
7. Drag and drop the file(s) create from step 3 into the project.
8. Follow the steps from [How-To](#how-to) as normal.
9. Add the `Unity Uploader` to your project as you would another template.
10. Re-import any missing asset bundles, plugins, and/or assets that you need.
11. _Reconfigure the navigation mesh layer, and Lighting (`Window > Rendering > Lighting Settings`), and any other lost properties as necessary._
12. That should be it! From now on use this new project for the template. If everything works and nothing is missing, delete `[original project name]_old` from your project directory.

<sup>b</sup> If managing multiple templates from a single project, **repeat this step & steps 2 - 3 for each scene in the project**.
