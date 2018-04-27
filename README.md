# Welcome to Visual Strategies for Neural Artistic Style Transfer

## Requirements: ##
* Laptop running Windows or MacOS
* Image editing software — any application you are comfortable with including mobile apps.

## Background ##
Neural artistic style transfer is a method for repainting images in the style of other images using a neural network. The algorithm is computationally intensive because it must be run about a thousand times to produce a decent picture. The bigger the picture, the longer this takes. In order to create rapidly, we'll run these computations on a remote graphics server. Some images work better together than others. You'll learn how to recognize and manipulate images that cause the neural network to produce personal outcomes. 

The [neural-style code](https://github.com/jcjohnson/neural-style) was written by Justin Johnson, a PhD student in the Stanford Vision Lab. His work implements ideas described in the foundational paper, [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576) (Gatys, Ecker, Bethge, 1993). The "AI" for this workshop runs on an Amazon EC2 P3 server. This configuration is specific to this workshop and will only work for the time you're here. Ask me how to replicate this process at home if you're interested.

## Neural-style requires three **inputs** before it can synthesize an **output**:

### 1. Content image
The pigeon was cut out of an original photograph and placed on top of a white background, strategically biasing (distorting) the neural net's understanding of the image
<br><img src="https://github.com/skinjester/visual-strategies/blob/master/pigeon2.jpg" width="300" vspace="16"/>

### 2. Style image
<img src="https://github.com/skinjester/visual-strategies/blob/master/06-klimt-sm.jpg" width="300" vspace="16"/>

### 3. Render script
This batch file automates the setup and rendering of neural style transfer images. **No programming experience is required.** Instead, we'll open the scripts I've provided and edit the file names to match the images we use. Later, we'll also change some parameter values to see the effect this has on the outcome. 

```Shell
# Replace this with the filename of your content image
CONTENT_IMAGE=content-4.jpg

# Replace this with the filename of your style image
STYLE_IMAGE=style-basket.jpg

# Parameters
STYLE_WEIGHT=8e3    # default = 5e2 | range 1e0 (1) to 10e5 (10000) 
CONTENT_WEIGHT=2e3  # default = 5e0 | range 1e0 (1) to 10e5 (10000) 
STYLE_SCALE=0.7     # default = 1.0 | range 0.1 to 2.0

### other stuff... (hidden for clarity)
```
### The Output
The server returns an image after completing the render script. Small renders take about a minute, so its easy to try new things. As an example, this pigeon style took 4 rounds of adjustments and evaluation before arriving at a final image. <br><img src="https://github.com/skinjester/visual-strategies/blob/master/tharkibo.jpg" width="300" vspace="16"/><br>_by Thea Boodhoo @tharkibo_

## Setup
Before starting you'll need to setup a working environment.  
- [Setup for macOS](https://github.com/skinjester/visual-strategies/wiki/Setup-for-macOS)    
- [Setup for Windows](https://github.com/skinjester/visual-strategies/wiki/Setup-for-Windows)   


