# Void Linux WSL Distro Launcher

This project is based on the [WSL Distro Launcher](https://github.com/Microsoft/WSL-DistroLauncher).
Its goal is to let you install Void on the WSL.

## Setup and Installation

You'll need Visual Studio. You'll definitely also need WSL enabled, though
version (1 or 2) should not matter. Make sure you have sideloading enabled in
developer options in Windows Settings.

1. Open DistroLauncher.sln in Visual Studio
2. In the "Void" project, open MyDistro.appxmanifest
3. Switch to the Packaging tab
4. Select "Choose Certificate"
5. Generate a certificate
6. Save
7. Download the latest x86 void ROOTFS tarball, then do the following:
  1. Unpack the .xz archive (so you're left with .tar)
  2. Repack the tarbal with gzip (so you get .tar.gz)
  3. Rename the archive to "install.tar.gz"
  4. Make a directory called x64 in the root of the project
  5. Place your install.tar.gz in it
8. In Visual Studio, make sure your build settings (dropdowns at the top) are
   set to "Release" and "x64"
9. Go to Build -> Deploy Solution
10. Open the start menu and search for "Void" (it is probably at the top already
    anyway, since it was recently installed) and run it
