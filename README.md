# OrthoMorph
Application of Image morphing on orthodontic before and after images

## Images
Pre Treatment            |  Post Treatment
:-------------------------:|:-------------------------:
<img src="img/ortho_init.jpg" width="300">  | <img src="img/ortho_fin.jpg" width="300" > 
 <img src="facemorph/angie_init.jpg" width="300">  | <img src="facemorph/angie_fin.jpg" width="300"> 

## Inspiration
Do you smile with your lips closed? Do you cover your mouth with your hand while you laugh? While many people have crooked teeth, if your teeth are a source of pain or embarrassment, braces are a solution you will definitely consider. More than [3.5 million children](http://www.bracesct.com/braces-for-kids#:~:text=Since%20a%20healthy%2C%20beautiful%20smile,(usually%20braces)%20each%20year.) and teens begin orthodontic treatment (usually braces) each year. Famous celebrities like Kendall Jenner, Angelina Jolie and Tom Cruise have had braces. A good smile boosts self-confidence and stays with you throughout your life. 

## What it does
The major problem orthodontists face is showing prospective patients how their teeth will transition from their current state to the final state. This gives patients surity and an idea of how they and their teeth are going to transform in the 1-1.5 years of the treatment duration. The usefulness of this technique is perhaps more for the education of medical students and orthodontic residents. Another application may be for the orthodontist to show to each other and their patients success and complications that can/will arise during the course of the treatment. Most importantly, people interested in getting braces can upload their dental images on a website and visualise how their teeth will reposition.

## How we built it
While image morphing is popularly used in movies for seemless transitions, I realised it could be applied in the field of orthodontics. I used upper lingual arch images of pre and post treatment available online. I built the morphed video using an algorithm for Image morphing called Mesh Warping. It utilises Delaunay triangulation for making a triangular mesh. Post this, affine transforms are applied on each triangle to get intermediate images. Intermediate images are obtained in steps of 0.1 from 0 to 1. These images are combined to give a video of the transition from the source to target image. 

## Challenges we ran into
Manually choosing corresponding points between the source and target image was cumbersome. Additionally I had to do a lot of trial and error to get a good morphing. I also had to figure out how to use the dlib library for facial features detection. 

## Accomplishments that we're proud of
Super proud of this idea and having a working video which shows the transformation from the pre-treatment to the post-treatment images! Medical applications of image morphing have not been applied in the field of dentistry, I plan to get into contact with professors asap and pursue this as a research project (and maybe publish a paper!? hopefully I'm not being to ambitious haha xD).

## What we learned
I got familiar with the opencv library. I ideated and learnt a different application of image morphing. Also understood how Machine Learning has been used in dlib library and the datasets it was trained on. 

## What's next for OrthoMorph
Building a software where the orthodontist can enter the pre-treatment and potential post-treatment image and show it to the prospective patient, like how we have for [celebrity face morphing](https://www.morphthing.com/). I see huge scope in research for this. Finite Element Methods can be applied on the mesh to back-calculate the wiring that needs to be done to apply the adequate force and get the required transformation. Deformations can be analysed quickly by comparing to ideal lingual arch scenario. Morphings will be done for all pre and post-treatment images, as shown [here](https://www.clubbraces.com/blog/2016/05/6-ways-broadening-your-dental-arch-will-give-you-a-dazzling-smile-2).

## Final Transition Video
The thumbnail provides a quick, low-resolution sample video of how the images will morph. This allows for checking to make sure major errors will not occur and also present prospective patients with a view of how their teeth will look in the final stage.
</br>
 <img src="video/morph.gif" width="300">  <img src="facemorph/angiegif.gif" width="300"> 



