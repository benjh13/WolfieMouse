# How to use IDE

You can download the IDE here: http://timor.atollic.com/truestudio/

## Add our existing project to the IDE
![](Ide_1.png)

After you clone our repository, launch Atollic TrueSTUDIO.
Select the workspace as the directory of the cloned repository.

![](Ide_2.png)

After launch we can see there is no project yet.

![](Ide_3.png)

To add existing project, Go to `File->Import`

![](ide_4.png)

In the prompt window. Select `General->Existing Projects into Workspace`

![](Ide_5.png)

Select one of our existing project, for example, `projects/test_atollic-studio`.

![](Ide_6.png)

Then you can see a project is added.

![](Ide_7.png)

Try compiling by clicking `Build Project` after you right click the project.

![](Ide_8.png)

After compiling you should see the success message like this.

![](Ide_9.png)

Then try to program this to your board by clicking `Debug As -> 1`

Now you should be able to debug just like other IDE. In the example project, the LED of the board should be blinking!

## How to created a new project in the IDE

Now it is time to make a simple blinking LED project.

![](ide2_0.png)

Go to `File -> New -> C++ Project`

![](ide2_1.png)

Type a project name and set a location, if you want to make a project in a specific location like the example, uncheck `Use default location`

![](ide2_2.png)

Set a hardware configuration as exactly the same above.

![](ide2_3.png)

For the software configuration, just leave it as it is (meaning not important)

![](ide2_4.png)

Set a debugger configuration as ST-LINK. ST-LINK is our debugger using. Then click `Finish`

![](ide2_5.png)

You could see there is auto-generated files in the project. We need to delete them.

Go to the project folder and delete `Drivers` and `src` folder.

![](ide2_6.png)

Then `clean project` first and go to `Properties`.

![](ide2_7.png)

In the properties, go to `C/C++ General -> Paths and Symbols`. Then in the ` Includes ` tab delete all Include directories in all languages.

![](ide2_8.png)

Go to `Source Location` Folder, and then click `Link folder` and the above graphic will be shown.

Select `source` folder in the top directory in our repository.

![](ide2_10.png)

Go to `Includes` tab. Let import our pre-made settings.

Click `Import Settings`...

![](ide2_11.png)

Select `path-and-symbols.xml` in `settings` folder.

![](ide2_12.png)

You should see the Includes and Symbols are updated.

![](ide2_13.png)

also, for main.cpp there is example main file in `settings` folder.

copy and past to the project folder. Then build it and debug!