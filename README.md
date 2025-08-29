# Fine-Tuning Flux.1-Schnell for Image Generation

This repository demonstrates how to fine-tune the **Flux.1-Schnell**
model for custom text-to-image generation tasks.\
The project leverages modern diffusion models and configuration-driven
training.

## 📂 Project Structure

    ├── data/                     # Training dataset (images + captions)
    ├── output/                   # Outputs after training (fine-tuned model, logs, samples)
    |   ├── config.yaml               # Configuration file for training (after fine-tuning)
    ├── Fine Tune Flux.1-Schnell.ipynb   # Jupyter Notebook for fine-tuning pipeline
    ├── requirements.txt          # Python dependencies
    └── README.md                 # Project documentation

## ⚙️ Setup

### 1. Create virtual environment

``` bash
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate    # On Windows
```

### 2. Install dependencies

``` bash
pip install -r requirements.txt
```

## 🚀 Fine-Tuning

You can fine-tune the model using the provided Jupyter Notebook:

1.  Open `Fine Tune Flux.1-Schnell.ipynb`\
2.  Update dataset path in cell 11 \
('datasets', [ \
                    OrderedDict([ \
                        ('folder_path', '/workspace/data'), # path dataset here\
                        ('caption_ext', 'txt'), \ 
                        ('caption_dropout_rate', 0.1),\ 
                        ('shuffle_tokens', False),\ 
                        ('cache_latents_to_disk', True),\ 
                        ('resolution', [1024]) \
                    ])\
                ]),\
3.  Run all cells to start training

Training outputs (fine-tuned checkpoints, logs, and generated images)
will be saved inside the `output/` folder.


## 📊 Results

-   Fine-tuned model weights are stored in `output/`\
-   Generated sample images are also saved in `output/samples/`\
-   Training logs can be reviewed for performance tracking

## 📌 Notes

-   Use a GPU with at least **12GB VRAM** for efficient training\
-   Adjust hyperparameters in `config.yaml` based on dataset size\
-   Dataset should include paired **images + captions** for best results

## 📜 License

This project is for research and educational purposes only.
