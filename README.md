# RStudio on Binder

## Overview

This repository contains the configuration files for running RStudio on
[Binder.org], a free service for running data science notebooks in the cloud.

## Instructions

### 1. Click to launch: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/januarharianto/rstudio_teaching/HEAD?urlpath=rstudio)

Binder will build the image and launch RStudio on R v4.2.0 and [RStudio
v2022.02.3](https://dailies.rstudio.com/version/2022.02.3+492.pro3/). Building
the image _should_ take a few seconds, but it can take up to 5 minutes if Binder
needs to build the image from scratch.

### 2. Upload data

Because this is a temporary environment, you will need to upload any data or
files you want to work on. You can do this by clicking on the "Upload" button in
the **Files** pane in the lower right corner of RStudio. If you are uploading a
folder, you will need to zip it first.

### 3. Run code

RStudio on Binder should work just like RStudio on your local machine.

## Frequently Asked Questions

!!! note Are my files saved when I close the session?

    No. This is a temporary environment, so any files you upload will be deleted when you close the session. To save your work you will need to select the files that you want to download (by checking the box next to the file or folder name) and then clicking on **More > Export**. RStudio will create a zip file of the files and the files will be downloaded to your local machine.

!!! note Can I install packages?

    Yes. Use the `install.packages()` function as usual. Keep your installation configuration in an `.R` script so that you can re-run it in a new session.

!!! note Is my personal information safe when using this service?

    **TLDR:** Yes, your information is safe. Binder.org does not ask for any personal information and *destroys* the RStudio environment when you close the session.

    **Long version**: The RStudio server is running on an isolated Kubertenes container that is destroyed when you close the session. As you do not have to log in or register to use the service, there is no way to track your activity. The only information that is stored is the URL of this GitHub repository, which is used to build the image. Any data you upload is also destroyed when the session is closed.

!!! note Can I use this service for my own projects?

    **Absolutely**. However please note that Binder.org is a free service and is not
    intended for long-term use, or for large datasets. If you are planning to
    use this service for a long-term project, you should consider using a paid
    service such as [RStudio Cloud](https://posit.cloud/) or run a local
    instance of RStudio on your own computer.

## Acknowledgement

Based on the [rocker/geospatial](https://hub.docker.com/r/rocker/geospatial)
image.

[Binder.org]: https://mybinder.readthedocs.io/en/latest/
