# MDETR -- Modulated Detection for End-to-End Multi-Modal Understanding
MDETR -- Modulated Detection for End-to-End Multi-Modal Understanding
Multi-modal reasoning systems rely on a pre-trained object detector to extract regions of interest from the image. However, this crucial module is typically used as a black box, trained independently of the downstream task and on a fixed vocabulary of objects and attributes. This makes it challenging for such systems to capture the long tail of visual concepts expressed in free form text. In this paper authors propose MDETR, an end-to-end modulated detector that detects objects in an image conditioned on a raw text query, like a caption or a question. They use a transformer-based architecture to reason jointly over text and image by fusing the two modalities at an early stage of the model. They pre-train the network on 1.3M text-image pairs, mined from pre-existing multi-modal datasets having explicit alignment between phrases in text and objects in the image. The creators then fine-tune on several downstream tasks such as phrase grounding, referring expression comprehension and segmentation, achieving state-of-the-art results on popular benchmarks. We also investigate the utility of our model as an object detector on a given label set when fine-tuned in a few-shot setting. They show that our pre-training approach provides a way to handle the long tail of object categories which have very few labelled instances. Authors' approach can be easily extended for visual question answering, achieving competitive performance on GQA and CLEVR.<br> 
The code and models are available at https://github.com/ashkamath/mdetr <br>
The paper is available at https://paperswithcode.com/paper/mdetr-modulated-detection-for-end-to-end/review/ <br>
## Architecture
<div align="center">
  <img src="https://production-media.paperswithcode.com/methods/Screen_Shot_2021-08-11_at_10.03.50_AM.png" width="1200" height="400"/>
</div> <br>

# SD INPAINTING
Stable Diffusion Inpainting is a latent text-to-image diffusion model capable of generating photo-realistic images given any text input, with the extra capability of inpainting the pictures by using a mask.<br>
This model is featured on the hugging face website (https://huggingface.co/runwayml/stable-diffusion-inpainting), where you can also find its use.<br>

# ABOUT
In the current notebook, we detect the desired objects by a query, e.g. 'find the largest object'. For this purpose we use MDETR. Then we create a mask of the detected object and generate a new object in place of this object using SD Inpainting model<br>

# HOW TO RUN THE NOTEBOOK LOCAL
1. Download the notebook and install requirement.txt . <br>
In this cell, you should create a custom prompt to locate the desired object <br>
2. In this cell you need to provide a path to you local folder with any images <br>
3. These cell can be skipped or, if you want to run it, you need to change all the patches in it. <br>
These cells are also an example of how you can run a diffusion model and generate a new photo with your own promt. In this way, you can create a custom photo.<br>
4. YOU MUST CHANGE ALL PATHS TO YOUR IMAGE IN  "plot_inference_results_mask" and "plot_inference_results" FUNCTIONS. <br>
5. Skip cells with !pip install <br>
NOTE: The entire notebook is sequential. You need to run the cells one at a time <br>
NOTE : If the gradio does not import, you need to rerun the notebook <br>
<br>

# HOW TO RUN THE NOTEBOOK IN GOOGLE COLAB
1. Download this notebook to Google Colab. All dependencies will be set automatically <br>
In this cell, you should create a custom prompt to locate the desired object <br>
2. In this box, you can download a zip folder of images from google drive or use the link provided <br>
3. These cells can be skipped or, if you want to run it, you need to change all the paths in it. <br>
These cells are also an example of how you can run a diffusion model and generate a new photo with your own promt. In this way, you can create a custom photo.<br>
4.IF PROVEDE YOUR OWN LINL TO IMAGES YOU MUST CHANGE ALL PATHS TO YOUR IMAGES IN  "plot_inference_results_mask" and "plot_inference_results" FUNCTIONS. <br>
NOTE: The entire notebook is sequential. You need to run the cells one at a time <br>
NOTE : If the gradio does not import, you need to rerun the notebook <br>
