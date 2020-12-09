# Image Analysis in Python - Basics

based on day 1 and day 2 of the following course:

https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis

by the Image Analysis Focused Interest Group of the Royal Microscopical Society (IAFIG-RMS) Python for Bioimage Analysis Course.

![RMS logo](/resources/image002small.png)

## Aim:
The aim of 4 afternoon course is to teach motivated students/staff the Basics of BioImage analysis in Python. 

## Target Audience:
Cell Biologists, Biophysicists, BioImage Analysts with some experience of basic microscopy image analysis. In addition, this course may be of interest to physical scientists looking to develop their knowledge of Python coding in the context of image analysis. This course is appropriate for researchers who are relatively proficient with computers but maybe not had the time or resources available to become programmers. Some prior experience of scripting or modifying scripts would be useful. We ask that all attendees complete a basic Python coding course before the course begins. Details of this will be sent to attendees which apply.

## Learning Outcomes: 
This course will give candidates knowledge of image analysis theory and algorithms:
* It will consolidate and extend their Python coding skills to cover topics relevant to bioimage analysis (see content below). 
* It will give them practise coding algorithms. 
* Candidates will experience developing pipelines which start with raw data and result in publication quality figures and will be able to apply this process in the future.

## Content:
Lectures will focus on Image Analysis theory and application. Topics to be covered include: Image Analysis and image processing, Python and Jupyter notebooks, Visualisation and Segmentation.The bulk of the practical work will focus on Python and how to code algorithms and handle data using Python. Fiji will be used as a tool to facilitate image analysis.  Research spotlight talks will demonstrate research of instructors/scientists using taught techniques in the wild.

## Prequisites
- Basic awareness of Fiji/ImageJ. You should be able to open images and do basic analysis, basic macro writing is advantageous.
- Python introductory course offered by the Max Planck Bioimaging network and 
- https://github.com/trasse/intermediate_python
- or
- : https://github.com/ChasNelson1990/python-zero-to-hero-beginners-course
  - If you've not done much Python in the past, you should work your way through the pre-requisite course (approx. 12-15 hr); however, those comfortable in Python may choose to skips components they are confident about.

## Organisers
Dominic Waithe and Gabriella Rustici.
### Co-organisers
Chas Nelson and Stephen Cross.
### Lecturers
Aurelien Barbotin (AB)  
Chas Nelson (CN)  
Dominic Waithe (DW)  
Ola (Alexandra) Tarkowska (OT)  
Mikolaj Kundegorski (MK)  
Stephen Cross (SC)  
Todd Fallesen (TD)  

## Timetable
#### Afternoon 1 (Image Processing and General Analysis):
- Introduction to course and structure. (DW)
- Images in Python (CN) ([practical notebook](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day01-image-processing-and-general-analysis/01_images-in-python/images-in-python.ipynb))
#### Afternoon 2 (General Analysis):

- Interactive demonstration: image processing in Python. (CN) ([practical notebook](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day01-image-processing-and-general-analysis/02_processing-in-python/processing-in-python.ipynb))
- Interactive demonstration: Fiji to Python. Visualisation (TF). ([overview](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/tree/master/sessions/day01-image-processing-and-general-analysis/03_fiji-to-python))
- Using ImageJ within Python (CN, [video](https://youtu.be/5q4vHM0zOLk))

#### Afternoon 3 (Segmentation):

- Segmentation (DW) ([pdf](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day02-segmentation-and-colocalization/01_segmentation/2019_IAFIG_Segmentation.pdf)) ([video lecture](https://youtu.be/cmOnOvbUUIk
  ))
- Practical (DW) ([practical notebook](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day02-segmentation-and-colocalization/01_segmentation/Segmentation%20practical.ipynb))

#### Afternoon 4 (Colocalization):

- Colocalisation and Registration (DW) ([pdf](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day02-segmentation-and-colocalization/02_colocalization/2019_IAFIG_colocalization_registration.pdf)) ([video lecture](https://youtu.be/cOrCz4qc8DI))
- Practical (DW) ([practical notebook](https://github.com/IAFIG-RMS/Python-for-Bioimage-Analysis/blob/master/sessions/day02-segmentation-and-colocalization/02_colocalization/2019_IAFIG_colocalization_practical.ipynb))

## How to use this repository

This repository contains the materials used during the course. We will create a new 'release' each time we run this course.

The following instructions assume you have installed the Python 3.7 version of Anaconda for you computer; see https://www.anaconda.com/distribution/#download-section for download links and instructions. They are also aimed a Jupyter Lab interface (which uses ipynb notebooks) and not the older Jupyter Notebook interface (which also uses ipynb notebooks).

To get the materials for your version of the course please download the zip for that release by going to clicking the 'X releases' link above. To get the latest materials please download the zip (using the green button above).

1. Unzip the downloaded file.
2. Open a terminal and navigate to the unzipped folder, e.g. `cd ./Python-for-Bioimage-Analysis/`.
3. Run `conda env create -f environment.yml`. This installs all the prerequisite packages for the course in a virtual environment called 'bioimage'.
4. Run `conda activate bioimage`. This moves you into the virtual environment.
5. Run `python3 -m ipykernel install --user --name=bioimage`. This makes this virtual environment available as a kernel in Jupyter lab.
6. Run `conda deactivate` to leave the virtual environment.
7. Start Jupyter Lab, either through Anaconda Navigator or by running `jupyter lab` in a terminal.

You will need to change the kernel for each notebook from the default 'Python 3' notebook to the 'bioimage' notebook. You can do this by clicking where it says 'Python 3' in the top right or bottom left of a Jupyter Lab window.

### Issues with %matplotlib widget

Using `%matplotlib widget` provides interactive elements for plots inside notebooks. However, it is still a young system and sometimes things don't work straight away. The following two issues may occur:

1. Instead of plots you see 'Canvas(...' or similar messages. In this case the jupyter-matplotlib (or `ipympl`) module has not properly installed/been enabled within Jupyter Lab. Completely shutdown Jupyter Lab and follow these instructions:
  * `conda install ipympl nodejs`
  * `jupyter labextension install @jupyter-widgets/jupyterlab-manager`
  * `jupyter labextension install jupyter-matplotlib`
  * `jupyter lab build`
  * Restart Jupyter Lab.
2. Instead of plots you see 'Loading widget...'. You probably just need to completely shut down Jupyter Lab and restart it.

### A Note on 'Releases'

For each time this course is delivered we will create a new release.
We will use a two number naming system, e.g. `v1.0`; this first number will be changed for each new delivery, the second number (after the point) will be updated when minor changes relating to that delivery are made.

As an example: the release for the first time this course was delivered is `v1.0`; however, this does not include the recordings for all lectures.
These will be added later as new versions, e.g. `v1.2`.
The second time this course is delivered, we will update the version number to `v2.0`.

A list of major releases will be kept updated in this file:

* `v1.*` - Materials for the course delivered 2019-12-09 -- 2019-12-13 at the Bioinformatics Training Room, Craik-Marshall Building, Downing Site, University of Cambridge, UK

