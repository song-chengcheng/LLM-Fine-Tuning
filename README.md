# LLM-Fine-Tuning
## 创建并激活虚拟环境

```bash
conda create -n LLM python=3.10 -y
conda activate LLM
```

## 下载LLaMA-Factory

```bash
git clone --depth 1 https://github.com/hiyouga/LLaMA-Factory.git
cd LLaMA-Factory
pip install -e ".[torch,metrics]"
```

## 下载模型

  1.安装依赖

  ```bash
  pip install -U huggingface_hub
  ```
  
  2.设置环境变量
  
   ```bash
   export HF_ENDPOINT=https://hf-mirror.com
  ```
  
  3.设置存储目录
  
   ```bash
   export HF_HOME=PATH
  ```
  
  4.用于显示当前设置的 HF_HOME 环境变量的值
  
   ```bash
   echo $HF_HOME
  ```
  
  5.下载模型
  
   ```bash
   huggingface-cli download --resume-download deepseek-ai/DeepSeek-R1-Distill-Qwen-7B
  ```

## LLaMA-Factory启动

```bash
llamafactory-cli webui
```

![](https://github.com/song-chengcheng/LLM-Fine-Tuning/blob/main/images/image.png)

## 训练
```bash
export NCCL_P2P_DISABLE=1
export NCCL_IB_DISABLE=1
```
