# Readme in English
# Knowledge Base Generation and Question Answering System based on LLM

## Create a virtual environment
Python 3.11 requires CUDA version 12 or above

## Install all dependencies

$ cd 2024lmcbise
$ pip install -r requirements.txt

## Download models
Required models include:

chatGLM2-6b
text2vec
You can download common open-source LLM and embedding models from the HuggingFace mirror website hf-mirror.com.
To download models, you need to install Git LFS first, and then run the following commands:

$ git lfs install
$ git clone https://hf-mirror.com/THUDM/chatglm2-6b
$ git clone https://hf-mirror.com/GanymedeNil/text2vec-large-chinese

## Modify configuration files
Add the absolute path of the model in model_config.py.

## Run the program

cd 2024lmcbise

Execute the cli_demo.py script to experience command-line interaction:


$ python cli_demo.py

Or execute the webui.py script to experience Web interaction:


$ python webui.py

Or deploy an API using fastapi:


$ python api.py

Experience the VUE-based front-end page after successfully deploying the API:

$ cd views
$ pnpm i
$ npm run dev

Project Reference: https://github.com/chatchat-space/Langchain-Chatchat

---
# Readme in Chinese

# Knowledge base generation and question answering system based on LLM

## 创建虚拟环境
python 3.11 cuda版本需要12及以上

## 安装全部依赖
$  cd 2024lmcbise
$ pip install -r requirements.txt 

## 模型下载
需要用到的模型有
chatGLM2-6b
text2vec
#可以去通常开源 LLM 与 Embedding 模型可以从 HuggingFace 的镜像网站hf-mirror.com下载。
#下载模型需要先安装 Git LFS ，然后运行

$ git lfs install
$ git clone https://hf-mirror.com/THUDM/chatglm2-6b
$ git clone https://hf-mirror.com/GanymedeNil/text2vec-large-chinese

## 修改configs配置文件
#在model_config.py中添加模型绝对目录。

## 运行程序

cd 2024lmcbise

执行 cli_demo.py 脚本体验**命令行交互**：

```shell
$ python cli_demo.py
```

或执行 [webui.py](webui.py) 脚本体验 **Web 交互**

```shell
$ python webui.py
```

或执行 [api.py](api.py) 利用 fastapi 部署 API

```shell
$ python api.py
```

## 或成功部署 API 后，执行以下脚本体验基于 VUE 的前端页面

```shell
$ cd views 
$ pnpm i
$ npm run dev
```

项目主要参考：https://github.com/chatchat-space/Langchain-Chatchat
