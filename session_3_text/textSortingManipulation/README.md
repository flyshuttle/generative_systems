# Generative_systems
Generative Systems for Art and Design course materials
 ©2020 Dan Buzzo
 www.buzzo.com

 Examples built in C++ using openFrameworks (openframeworks.cc)

## 3 Text and narrative

* Techniques: text sorting, automatic and generative poetry, interactive story structure
* Ideas: Grammar and variation
* Demo: Markov chain text, lexical searches. 
  * nGrams and generating models for markov chains
  * screenshot-automaticWriting.png
* Examples: TSR chooose your own adventure, exquisite corpse, 

https://github.com/danbz

• Introduction to text processing
• Semantics

see also
• oF_root/examples/strings/sortingExample & regularExpressionExample
• oF_root/examples/input_output/loadTextFileExample & imageLoaderWebExample

* portions modified from oF sortingExample

### Learning Objectives

This example demonstrates how to sort a vector alphabetically, by word length or by word occurence. It shows you how to..
* load words from a file into a vector
* create custom sorting functions
* sort the vector using the function ```ofSort()```
* load text from file using fileDialog
* load text from a remote URL on the web
* scale the line height based upon character order
also

This openFrameworks example demonstrates how to load a txt file from the web  

In this example, pay attention to the following code:

* Request to load an image using ```ofLoadURLAsync``` which passes the url, and a name for the request
* Handle the response from the request using ```void ofApp::urlResponse```
* Determine information about the fullfilled request by inspecting the status code ```response.status``` and the request name ```response.request.name```
* On exit of the application, unregister the application from being notified of the URL request completion using ```ofUnregisterURLNotification```
*

### Expected Behavior

When launching this app, you should see a screen with words circularly arranged on the right side.

Instructions for use:

* Press keys from ```1``` to ```4``` to switch sorting algorithms.
* press ```l``` to open file dialog to lad text file from disk
* press ```f``` to toggle fullscreen display

### Other classes used in this file

This Example uses the following classes:

* http://openframeworks.cc/documentation/graphics/ofTrueTypeFont/
* http://openframeworks.cc/documentation/utils/ofUtils/

![screenshot](screenshot-textSortingManipulation.png)

nb. on RaspberryPi - if running oF app alongside xWindows desktop the file dialog is created under/alongside the oF Window.This is because oF on raspberryPi is meant to run outside of xwindows as it directly interfaces the GPU