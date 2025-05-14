# *Animated Story Video Generator*

This project generates an *animated story video* using *Google Colab* and *Gemini AI Studio. The code takes a **story theme* as input and automatically generates:
- *Story sequences* with scenes.
- *Images* for each scene using *Google Imagen*.
- *Audio narration* for each scene using *Google Live API*.
- A *final animated video* combining the images and audio.

## *How It Works*
1. The code uses *Gemini AI Studio API* to generate a sequence of scenes based on a provided story theme.
2. *Google Imagen* generates images for each scene based on scene descriptions and character details.
3. *Google Live API* generates audio narration for each scene.
4. The code uses *MoviePy* to combine the images and audio into a final video.

## *How to Run the Code*
1. First, create a *Gemini AI Studio* account and generate an *API Key*.
2. Open the notebook in *Google Colab* and set your *API Key*.
3. Run the cells in sequence to generate story scenes, images, audio, and the final animated video.
  
