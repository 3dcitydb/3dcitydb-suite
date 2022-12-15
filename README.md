3D City Database Suite
======================

This is an umbrella repository for the 3D City Database and the associated software tools to import,
export, manage, analyse, and visualize virtual 3D city models based on the 3D City Database.

The 3D City Database and each software tool are managed in separate repositories and follow their own
development and release cycles. The purpose of this repository is to bundle the separate components at one
place and to create regular releases of the entire suite. A suite release contains the most recent
and stable versions of all components at the time of the release and is assigned its own version number.

With every release of the suite we also publish an installer that lets you install the Importer/Exporter,
the 3D City Database scripts, the 3D Web Map Client, and Importer/Exporter plugins on your local machine.

Latest release
--------------
The latest stable release of the 3D City Database Suite is 2022.2.0.

You can download the installer for the latest release as well as previous releases from the
[releases section](https://github.com/3dcitydb/3dcitydb-suite/releases). A complete and comprehensive user manual
for this release is available [online](https://3dcitydb-docs.readthedocs.io/en/version-2022.2/).

Contributing
------------
If you want to file bugs, contribute code or propose a new feature for a specific software component,
please create a GitHub issue or a pull request **in the repository of the corresponding software component**.

Building a 3D City Database Suite installer
-------------------------------------------
This repository lets you build your own installer for the Importer/Exporter including the 3D City Database scripts,
the 3D Web Map Client, and Importer/Exporter plugins. We use [Gradle](https://gradle.org/) as build system.
To build the installer from source, clone the repository to your local machine and run the following
command from the root of the repository.

    > gradlew buildImpExpInstaller

The script automatically clones the repositories of all required software components and downloads all
mandatory dependencies for building the software. So, make sure you are connected to the internet. The build process
runs on all major operating systems and only requires a Java 8 JDK or higher to run.

If the build was successful, you will find the Importer/Exporter installer under `build/distributions`.

You can adapt the `.gitmodules` file in the root of the repository if you want a specific branch of a software
component to be used in the build process. Make sure that the versions of the software components from the branches
you have selected are compatible with each other.