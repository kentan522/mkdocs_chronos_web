# Preparing the Requirements
Before anything, clone the branch's repository as follows:

```bash
git clone -b chronosweb_core https://github.com/tsl-imperial/Chronos.git 
```

This branch will be cloned into a directory called 'Chronos' in your current working directory. Feel free to rename this directory if you wish.

## Conda Environment
An `environment.yml` file is included in the repository. Do follow the steps below to reproduce the appropriate environment for running the web interface locally. 

Firstly, ensure that your current working directory resides in the same folder as the repository. Then, do the following steps on your terminal:

*Step 1: Reproducing the environment*

```bash
conda env create -f environment.yml
```

*Step 2: Activating the environment*

```bash
conda activate chronos_web
```

Your environment should now be configured to run the web interface locally later! You may check if this is valid by running `conda list` to see if you get a long list of installed dependencies.

## External Packages (FFmpeg)
FFmpeg is a multimedia framework that is able to decode and encode video data. For our case, the framework is used to send video byte data to the web interface to be streamed. FFmpeg will have to be installed on your device to allow the web interface to stream the pygame visualisations.

To install FFmpeg:
1. Navigate to [FFMpeg's Official Website](https://ffmpeg.org/download.html).
2. Choose your device's OS and download FFmpeg version 4.4.
3. Open the executable file (if any) to install it on your device.
4. Remember to restart your terminal before running app.py later.
