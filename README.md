 # ![MotorMC](https://files.garet.holiday/motormc/logo1.png) [![](https://github.com/garet90/MotorMC/actions/workflows/build.yml/badge.svg)](https://github.com/garet90/MotorMC/actions/workflows/build.yml) [![](https://app.codacy.com/project/badge/Grade/2715a20b263142c9b5bd25fab473cd76)](https://www.codacy.com/gh/garet90/MotorMC/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=garet90/MotorMC&amp;utm_campaign=Badge_Grade)
***Note: MotorMC is currently in development and is not ready for production servers.***
MotorMC is a blazing fast, multi-threaded, asynchronous version of Minecraft that aims to handle many players on a single world while still providing an experience as close to vanilla Minecraft as possible.
## About
Unlike vanilla Minecraft, MotorMC is written in C--the same programming language your operating system is written in--to get maximum performance by removing the overhead of the Java Runtime Environment. Additionally, MotorMC does not utilize a garbage collector meaning each piece of memory is manually allocated and freed, allowing for extremely low memory usage.
### Multi-threading
In vanilla Minecraft, everything resource-intensive runs on a single thread. But, as newer processors have upwards of 8, 16, and even 32 cores, this leaves the processor mainly unutilized. MotorMC seeks to remedy this by splitting up all the work, such as block updates and entity calculations, between all of the cores. Other third-party Minecraft implementations have attempted this in the past, usually by splitting the world into pieces and assigning each piece to a different thread, but this can be grossly inefficient at times. By using a job pooling and a main-thread worker-thread model, jobs can be efficiently distributed to run every task in parallel.
### Plugin API
MotorMC is designed with plugin compatibility in mind. There is already a very experimental API that allows for the same drag-and-drop plugin experience found on Spigot and Paper. A wiki outlining the API and its use will be made eventually.
## Downloading
Currently, this project utilizes GitHub Actions to build binaries. These binaries should work out-of-the-box with Windows, Ubuntu, and MacOS. To download a binary, navigate to the "Actions" tab, click on the most recent successful build (the ones with green checkmarks next to them), scroll down to "Artifacts", and download the one that is compatible with your system. *Note: you WILL need a Github account to download MotorMC*
