# Answering_support_tickets_with_huffingface

Objective : Evaluate huffing face with support tickets

On Mac OSX with M2 proc, follow the process

1. compile llama

git clone https://github.com/ggerganov/llama.cpp
cd llama.cpp
make

2. get the llama model

By applying on meta ai and accept the license, provide email address. Meta will send download link in the email.
download https://github.com/facebookresearch/llama/blob/main/download.sh
move it to llama.cpp/models
chmod +x ./download.sh
run it
paste the URL received from meta.ai email
choose 13B-chat

3. intall environment and dependencies

python3.10 -m venv ~/.virtualenvs/venv-310-llama
source ~/.virtualenvs/venv-310-llama/bin/activate
pip install torch numpy sentencepiece

4. convert to ggml format

python3.10 convert.py --outfile ./models/llama-2-13b-chat/ggml-model-f16.bin --outtype f16 ./models/llama-2-13b-chat

## Alternate way

use the huggingface_hub to download the llama-2-13b-chat

Enjoy )))
