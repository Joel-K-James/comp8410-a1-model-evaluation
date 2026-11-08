**Joel Kuzhikalavayalil James — 49019457**  
**COMP8410 Advanced Topics in Artificial Intelligence**

## About my project

My project is an evaluation of eight models on four convenience-retail tasks, informed by my experience working at Reddy Express. I put SDXL and Kandinsky to the test for product background replacement, Qwen3 and SmolLM3 for fielding staff questions, VAE and RealNVP to detect transaction anomalies and CLIP and SigLIP2 for catalogue recognition.

I collected the product images from the Woolworths online catalogue. As for the staff questions and reference material they are fictional, and the transaction data is synthetic. None of the work is based on confidential company or customer records and it does not speak to official Reddy Express policy.

## Running the notebooks

The experiments were done in Google Colab with a Tesla T4 GPU. To get around computational constraints I have used individual notebooks and moved shared inputs and any saved outputs via ZIP files.

In Colab open the notebook and make sure a T4 GPU is selected for the model ones. Follow the cells in sequence and execute the installation ones where they appear. You will need the packages and model checkpoints. The notebooks are built on PyTorch, Transformers, Diffusers and the like the commands to install them are there.

A new runtime should be used for every model notebook. If you are running Pairs 1 and 4 for the first time, upload the original product images to `/content/products_images` as they are named.

## Order of execution

Each pair is to be run on its own:

- **Pair 1:** `01a_sdxl` then `01b_kandinsky` then `01c_pair1_evaluation`
- **Pair 2:** `02a_qwen` then `02b_smollm` then `02c_pair2_evaluation`
- **Pair 3:** `03a_vae` then `03b_realnvp` then `03c_pair3_evaluation`
- **Pair 4:** `04a_clip` then `04b_siglip2` then `04c_pair4_evaluation`

They are all `.ipynb` files. At the end of the first notebook in a pair download the resulting ZIP and when asked put it into the second one. Do the same with the second notebook’s ZIP for the evaluation. Be sure to save your downloaded files before you close Colab since the storage is not permanent.

## My saved results

I included the saved output, configurations, CSVs and figures for each pair in their respective folders. The report has the details on what was found and any limitations.

New runs can yield different outcomes. With Pair 1 the batch IDs in the evaluation notebook will have to be updated. Any change to the saved outputs means the visual ratings in Pair 1 and the answer assessments in Pair 2 will require a fresh look.

Thank You.