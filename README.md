# computer_graphics_finalproject
Final project of the computer graphics course @ ucsp

---

**As to last change, way back in June.**

![Img_current_state](./_img/deferred_lighting.png)

**The report I made for the last presentation is [here](https://ts/cg/)**

## Cloning the project

The project depends on some libraries, which are added as submodules. Make sure you clone the project with the --recursive option, in order to get the dependencies from other repositories.

  git clone

## Build steps

I've test it with both Windows 10 and Ubuntu 16.04. The cmake file should work for other systems as well. In case it doesn't, just send me a message to wilsanph@gmail.com .

Also, make sure you are using an out of place build, by making a build directory and compiling the code there.

	mkdir build
	cd build
	cmake-gui or cmake OPTIONS ..

### Windows



### Linux

Testedi n Ubuntu 16.04, using g++ and makefiles. I've been having trouble making bullet a submodule and compiling it alongside the project, so the best way is to install bullet separately. The default configuration tries to search if Bullet was installed. If not, it falls back to the submodule. Unfortunately, I still can't find the issue with the build when using as a submodule, but will in a future release.

To build, just run ** cmake .. ** from the build directory.

### Running the demos

The current demo I have is the testScenario demo. Depending on your platform, just set it as a startup project ( visual studio ), or just run the generated binary in the build directory ( linux )

