# Overview

![pandemi](image/closed.gif)![sad](image/sad.gif) 

On the ILO (International Labor Organization) [report](https://www.ilo.org/wcmsp5/groups/public/---dgreports/---dcomm/documents/briefingnote/wcms_755910.pdf), it is predicted that at least 490 million workers have lost or reduced their working hours due to the Covid-19 pandemic.

Including here in Indonesia, many people have lost their source of income due to this pandemic. But not a few are trying to find new opportunities by opening small businesses. Various ways have been done to promote their business and of course social media has become a favorite platform to use. Instagram as one of the social media with the largest users in Indonesia is the main choice.

One of Instagram's great features for promotion is **Instagram Story** with various interesting **Filters**. In this tutorial we will try to create a **Filter** which can be used for promotion. This **Filter** will be in the form of a **Promo Card** which can be easily modified with an image or photo that the user has prepared himself for each promotion program.

We try to design this tutorial to be applied by users who are new to coding or have never even used **Spark AR Studio**, so hopefully it can help those who are looking for new opportunities in the midst of this pandemic.

This tutorial will cover 3 main things:

* Preparation and how to install **Spark AR Studio**
* Create a simple **Filter** in the form of a **Promo Card** with the **Gallery Texture** feature, where later the user can use their own image or photo on the **Filter**.
* Testing and the steps to publish **Filter** that we have created.

We hope that after following this tutorial you will be able to create your own filter that works well and managed to publish it.

# ![list](image/list.gif) Installing Spark AR Studio

**Spark AR Studio** is an augmented reality platform for Mac & Windows that allows us to easily create AR effects for mobile cameras. In this section we will prepare the things needed for the use of **Spark AR Studio**.

![prepare](image/prepare.gif) 

## Requirements
To install **Spark AR Studio** there are several things we need to prepare.

### Hardware
**Spark AR Studio** requires a PC with the following minimum specifications
* Minimum Operating System Windows 10 (64 bit) or MacOS 10.14+
* 4GB minimum RAM

More detailed specifications can be seen on the page https://sparkar.facebook.com/ar-studio/learn/downloads/#system-requirements

### Account
In order to use **Spark AR Studio** and publish the **Filter** that we are going to create, several accounts are required:
* Facebook account, to log in and use **Spark AR Studio** and organize the projects that we will publish.
* The Instagram account that was connected to the Facebook account, for testing and publishing the **Filter** that we created.

### Download Installer
If all the requirements have been met, now we can start installing **Spark AR Studio** by downloading the latest version at

https://sparkar.facebook.com/ar-studio/learn/downloads/#spark-ar-studio

When this tutorial was created, the latest version in use is v98. After successfully downloading the installer, please install it according to the steps shown.

### Facebook login
The first thing that is displayed when we open **Spark AR Studio** is a Facebook account login popup, fill it with your account data and then you can use **Spark AR Studio**.

![login](tutorial_images/00_login.PNG)

To logout **Spark AR Studio** from the current account, you can do it after opening the project by: clicking **File** then selecting **Logout**.

This is the end of the first part of the total 3 part tutorial. You have successfully prepared **Spark AR Studio** to create **Filters** which will be discussed in the second part of this tutorial.

![goodjob](image/goodjob.gif) 

# ![list](image/list.gif) Create a New Project

In this section we will start to create a Filter project.

![start project](image/startproject.gif) 

Please open **Spark AR Studio** which is already installed, the initial appearance of **Spark AR Studio** is a list of some of the templates provided, and there are several tutorials that you can try yourself later.

![homepage](tutorial_images/01_homepage.PNG)

## Opens Blank Project

For now we'll start by creating a new project from scratch.

Click **Create New** > **New Project**.

A popup will appear for the project types you can create. Since at this point we will learn from scratch, choose **Blank Project**.

![project baru](tutorial_images/02_new_project.gif)

## Main Display of Spark AR Studio
**Spark AR Studio** will open a new window which will become our workarea. If you pay attention, our workarea is divided into several main areas.

![mainview](tutorial_images/03_Main_View.PNG)

- A is the **Scene** panel. **Scene** panel is useful for arranging the order of objects that we will use. Ambient Light and Directional Light have been prepared by default. For this project we will just ignore the two light objects.
- B is the **Assets** panel. We will use the **Assets** panel to organize the files that we use in the project, such as images and materials.
- C is the **View** panel. In the middle section will be the main work area where we can directly view and edit the position and size of objects in our project.
- D is the **Properties** panel. On the right side, there is a **Properties** panel which can be used to adjust the settings of the objects we use.

## Added Face Tracker
Detecting faces is the main thing we need to make this **Filter**, this feature is very easy for us to make because **Spark AR Studio** has provided several types of trackers including **Face Tracker**.

To use Face Tracker on the **Scene** panel click the **Add Object** button which is on the lower right side then select **Face Tracker** then click **Insert**.

![add face tracker](tutorial_images/04_add_facetracker.gif)

**Face Tracker** object will be automatically added to hierarchy in **Scene** panel.
If desired, you can also rename the object that we created by double-clicking or by right-clicking then select **Rename**.

## Adding Plane Objects
After the Face Tracker, now we need an object that will be the place to display our filter image. We are going to add Plane object

To add a **Plane** we click the **Add Object** button on the **Scene** panel, then select **Plane** then click **Insert**.

![add plane](tutorial_images/05_add_plane.gif)

The **Plane** object has been added to the **Scene** panel and is also visible in the **View** panel. However, the **Plane** object is still not following the facial movements, we will fix it in the next step.

![plane not move](tutorial_images/06_plane_not_move.gif)

## Rearrange Object Hierarchy
To make the **Plane** object move with the face's movement, we need to rearrange the object hierarchy in **Scene**. We need to move **Plane** into **Face Tracker** in order to move along with facial movements.

To move it, on the **Scene** panel drag and drop the **Plane** object into the **Face Tracker** object.

![drag and drop](tutorial_images/07_plane_heriarchy.gif)

And as a result, the **Plane** object moves according to the facial movements.

![plane moving](tutorial_images/08_plane_moving.gif)

## Set Object Position
If we notice that the position of the **Plane** object covers the face, we need to adjust the position according to what we want. There are several ways that can be done, you can directly move the object through the **View** panel or by using the input on the **Properties** panel located on the right side of the screen.

### Using the View Panel
Moving objects via **View** can be done by drag the existing arrow lines. To make it easier to move objects, we can **Pause** the camera preview by pressing the pause button on the left side of the screen.

![pause](tutorial_images/09_pause_cam.gif)

And to move, just click the object on the **Scene** panel and on **View** panel drag the object's arrow line to the desired position.

![move arrow](tutorial_images/10_move_plane_arrow.gif)
