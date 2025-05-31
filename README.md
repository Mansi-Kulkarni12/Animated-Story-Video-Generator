# AI Story Animator

This project is a Python-based Jupyter Notebook that uses **Google's Gemini and Imagen AI models** to automatically generate and animate short stories from a simple theme. It's a fantastic showcase of how AI can be used for creative content production, from writing the story to generating its visuals and audio.

---

## ✨ Features

* **AI Story & Scene Generation:** Uses **Gemini** to create a multi-scene narrative, including specific prompts for images, audio text, and consistent character descriptions.
* **Consistent Visuals:** Ensures characters and art style are maintained across scenes via detailed prompts for **Imagen 3.0**.
* **Dynamic Image Creation:** Generates unique images for each story part using **Imagen 3.0**.
* **Automated Audio Narration:** Synthesizes narration or dialogue for each scene using **Google's Live API (Text-to-Speech)**.
* **Full Video Composition:** Combines all generated images and audio into a complete, synchronized animated video (`.mp4`) using `moviepy`.

---

## 🛠️ Technologies Used

* **Google Gemini API:** Story segmentation, text generation.
* **Google Imagen API (Imagen 3.0):** Text-to-image synthesis.
* **Google Live API:** Text-to-speech.
* **Python:** Core programming language.
* `moviepy`: Video editing.
* `Pillow`, `numpy`, `nest_asyncio`, `json`.

---

## 🚀 How to Run

This project is designed to be run in a **Jupyter Notebook environment** (like Google Colab).

### Prerequisites

1.  **Jupyter Notebook Environment:** Access to Google Colab, Jupyter Lab, or Jupyter Notebook.
2.  **Python 3.8+**.
3.  **Google Cloud Project** with **Gemini API** enabled.
4.  **Google API Key:** Obtain a Google API Key from your Google Cloud project credentials.
    * Ensure your API key has access to the **Gemini (generative models)** and **Imagen (Image Generation)** APIs.

### Installation & Setup (within the Notebook)

1.  **Open the Notebook:** Open the notebook file in your chosen Jupyter environment (e.g., Google Colab).
2.  **Install Dependencies:** Run the following cell at the beginning of the notebook to install all necessary libraries:

    ```python
    %pip install -q google-genai moviepy Pillow nest_asyncio
    ```

3.  **Set Up Your API Key:** You need to provide your Google API Key within the notebook. The most secure way in Google Colab is to use the `userdata` module. Run this cell in your notebook:

    ```python
    from google.colab import userdata
    import os

    os.environ['GOOGLE_API_KEY'] = userdata.get('GOOGLE_API_KEY')
    ```

    * **To add your API Key to Colab Secrets:**
        1.  In Google Colab, click the **key icon** (🔑) in the left sidebar to open "Secrets".
        2.  Click "Add new secret".
        3.  Set the **Name** to `GOOGLE_API_KEY`.
        4.  Paste your actual Google API Key into the **Value** field.
        5.  Make sure "Notebook access" is toggled ON.

### Execution

Once the dependencies are installed and your API key is set up in the notebook, simply run all the cells in the notebook sequentially. The notebook will prompt you for the story theme and number of scenes, then generate and save the animated video.
