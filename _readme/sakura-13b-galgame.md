## Localhost

Install Python 3.10. I used [Python 3.10.6](https://www.python.org/downloads/release/python-3106/).

Install [CUDA Toolkit](https://developer.nvidia.com/cuda-toolkit), I use `CUDA 12.1.0`. Check it:

```sh
nvcc -V
echo %CUDA_PATH%
echo %CUDA_PATH_V12_1%
```

Refer to [Start Locally](https://pytorch.org/get-started/locally/), install `torch`:

```sh
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

If you download `torch-2.2.2+cu121-cp310-cp310-win_amd64.whl` from https://download.pytorch.org/whl/torch:

```sh
pip3 install ...\torch-2.2.2+cu121-cp310-cp310-win_amd64.whl
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

Then:

```sh
pip3 install -r requirements.llamacpp.txt
```

Download model from [Hugging Face](https://huggingface.co/SakuraLLM). Here, I use [sakura-13b-lnovel-v0.9b-Q2_K.gguf](https://huggingface.co/SakuraLLM/Sakura-13B-LNovel-v0.9b-GGUF/blob/main/sakura-13b-lnovel-v0.9b-Q2_K.gguf) as an example.

Used as command:

```sh
python translate_novel.py --model_name_or_path ...\Sakura-13B-LNovel-v0.9b-GGUF\sakura-13b-lnovel-v0.9b-Q2_K.gguf --trust_remote_code --model_version 0.9 --llama_cpp --text_length 512 --data_path _input.txt --output_path _output.txt
```

Used as API:

```sh
python server.py --model_name_or_path ...\Sakura-13B-LNovel-v0.9b-GGUF\sakura-13b-lnovel-v0.9b-Q2_K.gguf --llama_cpp --model_version 0.9 --trust_remote_code --no-auth
```

## Reference

- [Python部署教程](https://github.com/SakuraLLM/Sakura-13B-Galgame/wiki/Python%E9%83%A8%E7%BD%B2%E6%95%99%E7%A8%8B)