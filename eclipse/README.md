Here are possible steps to set-up [Eclipse CDT](http://eclipse.org/cdt) to work on OLA.

1. Clone the OLA repository as usual outside of Eclipse (you could also use
   [EGit](http://eclipse.org/egit), but it's not covered here):

   `git clone git@github.com:OpenLightingProject/ola.git`


2. Run `autoreconf -i ` to generate the configure script as usual, and run your favorite configure line (e.g. `./configure CFLAGS="-g3 -O0"` for development).
2. Create a new project: **File** > **New** > **Project**... and choose **Makefile Project with Existing Code** under **C/C++**.
3. Choose the **Project name** as you wish (e.g. OLA) and point the **Existing Code Location** to your cloned repository.
4. In **Toolchain for Indexer Settings**, choose the toolchain you use for building OLA.

The indexer will take about a minute to do its work. To build the project, choose **Project** > **Build Project** from the top menu. This essentially runs make in the project's directory. If you chose to do an out-of-tree build, you can specify the build directory in the project properties.

To install the formatter settings:

1. In the project properties, go to **C/C++ General** > **Formatter**.
2. Check **Enable project specific settings**.
3. Browse and select OLA.xml from this repository.
