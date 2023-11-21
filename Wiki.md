# Setting Up Environment
The quickest way to test run the notebook demo apps on your local machine is to create a Conda envinronment and start running the Jupyter notebook as follows:

```
conda create -n llama-demo-apps python=3.8  
conda activate llama-demo-apps  
pip install jupyter  
cd <your_work_folder>  
git clone https://github.com/facebookresearch/llama-recipes  
cd llama-recipes/llama-demo-apps  
jupyter notebook  
```
You can also upload the notebooks to Google Colab.  

# Running Llama2 Locally
To run Llama2 locally using llama-cpp-python, first open the notebook HelloLlamaLocal. Then replace <path-to-llama-gguf-file> in the notebook HelloLlamaLocal with the path either to your downloaded quantized model file here (https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF/tree/main) -links to other models are provided several lines below in the "Other models" section-, or to the ggml-model-q4_0.gguf file built with the following commands:  

```
git clone https://github.com/ggerganov/llama.cpp  
cd llama.cpp  
python3 -m pip install -r requirements.txt  
python convert.py <path_to_your_downloaded_llama-2-13b_model>  
./quantize <path_to_your_downloaded_llama-2-13b_model>/ggml-model-f16.gguf <path_to_your_downloaded_llama-2-13b_model>/ggml-model-q4_0.gguf q4_0  
```

# Other models
https://huggingface.co/TheBloke/Llama-2-13B-chat-GGUF/tree/main  
https://huggingface.co/TheBloke/Llama-2-70B-Chat-GGUF/tree/main  

# Considerations
ai.meta:  
The Llama models thus far have been mainly focused on the English language. We are looking at true multi-linguality for the future but for now there are a lot of community projects that fine tune Llama models to support languages.  

medium:  
The LLaMA model is a foundation language model that was trained on 20 different languages. Yet, the vast majority of the training data used is in English, with all other 19 languages making up only a small percentage of the training data.

# Related links
https://github.com/facebookresearch/llama-recipes/tree/main/demo_apps  
