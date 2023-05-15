# LocalAI-Retraining of alpaca-lora
A guide to local AI training based on the Alpaca-Lora model in preparation for retraining.

### Local Setup

 Install dependencies
```
pip install -r requirements.txt
```
    
Open the project folder and find the "requirememts.txt" file location. Run the command prompt at this location, and then run this code at the command prompt. Note that to use pip you need to install python locally in advance. Please use python3.8.


### Training (`finetune.py`)

We don't recommend using finetune.py if we only have CPU, this is for users with GPU.


### Inference (`generate.py`)

```
.launch(server_name="0.0.0.0", share=True)
```
Change "share" to True in "generate.py".

```
base_model: str = "huggyllama/llama-7b",
lora_weights: str = "tloen/alpaca-lora-7b",
```
Make sure to select the model you want to run and set the weights. You can add or modify parameters here "def main". Whatever you like.

### Run "generate.py"

 ```
 python generate.py
 ```
Open and run this code in the file "generate.py" where it exists. Please always pay attention to the operation of the computer including temperature, memory usage. This will take some time to run the code. Once this is done, the command line prompt will provide an address that the user can open in a browser and then try to use the trained AI.

### Instruction selection

Locate the "alpaca_data.json" file. Please use the "instruction" and "input" inside to test the output.



