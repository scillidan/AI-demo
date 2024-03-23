## Localhost

```sh
python310 -m venv venv && venv\Scripts\activate.bat
pip install -r requirements.txt
pip install -e .
python -m unidic download
```

```sh
melo "Hello" output.wav --language EN
```

Start with webui:

```sh
pip install gradio==4.21.0
python melo/app.py
```

## Reference

- [运行web_demo_gradio.py报gbk解码错误，cli和streamlit则可以正常运行](https://github.com/THUDM/ChatGLM3/discussions/1009)