# Small LLM Tests

For laughs and giggles I wanted to see how well my super weak laptop without
dGPU can run LLMs, using the benchmark feature of Koboldcpp.

## Rules

Only models that fit inside 5.3GB RAM (7.8GB total, windows taking 2.5GB)
and are available for download on [HuggingFace](https://huggingface.co) are
allowed.

I limit myself to the following GUFF authors (in order of preference):

1. unsloth
2. mradermacher
3. DevQuasar

If supported context size is larger than 8192, I use 8192. If lower, I use
that value.

## Models

### Tested

For each model I use different context sizes. See Models table.

**Model**                    | **Type** | **Params** | **Quants** | **Context** | **Link**
---------------------------- | -------- | ---------- | ---------- | ----------- | --------
Deepseek R1 Distill Qwen     | Hybrid   | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/DeepSeek-R1-Distill-Qwen-1.5B-GGUF?show_file_info=DeepSeek-R1-Distill-Qwen-1.5B-Q8_0.gguf)
MobileLLM R1                 | Instruct | 360M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-360M-GGUF?show_file_info=facebook.MobileLLM-R1-360M.f16.gguf)    
MobileLLM R1                 | Instruct | 950M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-950M-GGUF?show_file_info=facebook.MobileLLM-R1-950M.f16.gguf)
Falcon3                      | Instruct | 1B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-1B-Instruct-GGUF?show_file_info=Falcon3-1B-Instruct.Q8_0.gguf)
Falcon3                      | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-3B-Instruct-GGUF?show_file_info=Falcon3-3B-Instruct.Q4_K_M.gguf)
Falcon H1                    | Instruct | 0.5B       | BF16       | 8192        | [link](https://huggingface.co/mradermacher/Falcon-H1-0.5B-Instruct-GGUF)
Falcon H1                    | Instruct | 1.5B       | BF16       | 8192        | [link](https://huggingface.co/mradermacher/Falcon-H1-1.5B-Instruct-GGUF?show_file_info=Falcon-H1-1.5B-Instruct.Q8_0.gguf)
Falcon H1                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-3B-Instruct-GGUF?show_file_info=Falcon-H1-3B-Instruct-Q4_K_M.gguf)

### To test

**Model**                    | **Type** | **Params** | **Quants** | **Context** | **Link**
-----------------------------| -------- | ---------- | ---------- | ----------- | --------
AceInstruct                  | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/AceInstruct-1.5B-GGUF?show_file_info=AceInstruct-1.5B.Q8_0.gguf)
Gemma 2 it                   | Instruct | 2B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/gemma-2-2b-it-GGUF?show_file_info=gemma-2-2b-it.Q8_0.gguf))
Gemma 3 it                   | Instruct | 270M       | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-270m-it-GGUF?show_file_info=gemma-3-270m-it-F16.gguf)
Gemma 3 it                   | Instruct | 1B         | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-1b-it-GGUF?show_file_info=gemma-3-1b-it-BF16.gguf)
Gemma 3 it                   | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3-4b-it-GGUF?show_file_info=gemma-3-4b-it-Q4_K_M.gguf)
Gemma 3n it                  | Instruct | 2B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3n-E2B-it-GGUF?show_file_info=gemma-3n-E2B-it-Q4_K_M.gguf)
GPT 2                        | Instruct | 355M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-medium-GGUF?show_file_info=gpt2-medium.f16.gguf)
GPT 2                        | Instruct | 774M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-large-GGUF?show_file_info=gpt2-large.f16.gguf)
GPT 2                        | Instruct | 1.5B       | Q8_0       | 1024        | [link](https://huggingface.co/mradermacher/gpt2-xl-GGUF?show_file_info=gpt2-xl.Q8_0.gguf)
Granite 3.1                  | Instruct | 1B A400M   | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-1b-a400m-instruct-GGUF?show_file_info=granite-3.1-1b-a400m-instruct.f16.gguf)
Granite 3.1                  | Instruct | 3B A800M   | Q4_K_M     | 8192        | [link](https://huggingface.co/DevQuasar/ibm-granite.granite-3.1-3b-a800m-instruct-GGUF?show_file_info=ibm-granite.granite-3.1-3b-a800m-instruct.Q4_K_M.gguf)
Granite 3.1                  | Instruct | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-2b-instruct-GGUF?show_file_info=granite-3.1-2b-instruct.Q8_0.gguf)
Granite 3.1                  | Hybrid   | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.2-2b-instruct-GGUF?show_file_info=granite-3.2-2b-instruct.Q8_0.gguf)
Granite 4.0                  | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-micro-GGUF?show_file_info=granite-4.0-micro-Q4_K_M.gguf)
Granite 4.0 H                | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-h-micro-GGUF?show_file_info=granite-4.0-h-micro-Q4_K_M.gguf)
Llama 3.1 Nemotron Nano v1.1 | Hybrid   | 4B    | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Llama-3.1-Nemotron-Nano-4B-v1.1-GGUF?show_file_info=Llama-3.1-Nemotron-Nano-4B-v1.1.Q4_K_M.gguf)
Llama 3.2                    | Instruct | 1B         | F16        | 8192        | [link](https://huggingface.co/unsloth/Llama-3.2-1B-Instruct-GGUF?show_file_info=Llama-3.2-1B-Instruct-F16.gguf)
Llama 3.2                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Llama-3.2-3B-Instruct-GGUF?show_file_info=Llama-3.2-3B-Instruct-Q4_K_M.gguf)
OLMo                         | Instruct | 1B         | F16        | 4096        | [link](https://huggingface.co/mradermacher/OLMo-1B-0724-hf-GGUF?show_file_info=OLMo-1B-0724-hf.f16.gguf)
OLMo 2                       | Instruct | 1B         | Q8_0       | 4096        | [link](https://huggingface.co/mradermacher/OLMo-2-0425-1B-GGUF?show_file_info=OLMo-2-0425-1B.Q8_0.gguf)
Phi 3.5 Mini                 | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Phi-3.5-mini-instruct-GGUF?show_file_info=Phi-3.5-mini-instruct.Q4_K_M.gguf)
Phi 4 Mini                   | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Phi-4-mini-instruct-GGUF?show_file_info=Phi-4-mini-instruct-Q4_K_M.gguf)
Phi 4 Mini                   | Thinking | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Phi-4-mini-reasoning-GGUF?show_file_info=Phi-4-mini-reasoning-Q4_K_M.gguf)
Qwen 2.5                     | Instruct | 0.5B       | F16        | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-0.5B-Instruct-GGUF?show_file_info=Qwen2.5-0.5B-Instruct.f16.gguf)
Qwen 2.5                     | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-1.5B-Instruct-GGUF?show_file_info=Qwen2.5-1.5B-Instruct.Q8_0.gguf)
Qwen 2.5                     | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-3B-Instruct-GGUF?show_file_info=Qwen2.5-3B-Instruct.Q4_K_M.gguf)
Qwen 2.5 VL                  | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-VL-3B-Instruct-GGUF?show_file_info=Qwen2.5-VL-3B-Instruct.Q4_K_M.gguf)
Qwen 2.5 Omni                | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen2.5-Omni-3B-GGUF?show_file_info=Qwen2.5-Omni-3B-Q4_K_M.gguf)
Qwen 3                       | Instruct | 0.6B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Qwen3-0.6B-GGUF?show_file_info=Qwen3-0.6B-BF16.gguf)
Qwen 3                       | Instruct | 1.7B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/Qwen3-1.7B-GGUF?show_file_info=Qwen3-1.7B-Q8_0.gguf)
Qwen 3                       | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen3-4B-Instruct-2507-GGUF?show_file_info=Qwen3-4B-Instruct-2507-Q4_K_M.gguf)
Qwen 3                       | Thinking | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen3-4B-Thinking-2507-GGUF?show_file_info=Qwen3-4B-Thinking-2507-Q4_K_M.gguf)
SmallThinker                 | Instruct | 4B A0.6B   | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/SmallThinker-4BA0.6B-Instruct-GGUF?show_file_info=SmallThinker-4BA0.6B-Instruct.Q4_K_M.gguf)
SmolLM 2                     | Instruct | 360M       | F16        | 8192        | [link](https://huggingface.co/unsloth/SmolLM2-360M-Instruct-GGUF?show_file_info=SmolLM2-360M-Instruct-F16.gguf)
SmolLM 2                     | Instruct | 1.7B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/SmolLM2-1.7B-Instruct-GGUF?show_file_info=SmolLM2-1.7B-Instruct-Q8_0.gguf)
SmolLM 3                     | Hybrid | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/SmolLM3-3B-GGUF?show_file_info=SmolLM3-3B-Q4_K_M.gguf)
TinyLlama v1.1               | Instruct | 1.1B       | F16        | 2048        | [link](https://huggingface.co/mradermacher/TinyLlama_v1.1-GGUF?show_file_info=TinyLlama_v1.1.f16.gguf)

## Testing environment

### Hardware

- Device: ASUS Vivobook E210MA
- CPU: Intel N5000
- GPU: Intel UHD 605
- RAM: 8GB DDR4 2400MHz (single-channel)
- SSD: Intel 660P 512GB

### Software

Windows:
- Edition: Windows 11 IoT Enterprise LTSC
- Version: 24H2
- OS build: 26100.6899
- Experience: Windows Feature Experience Pack 1000.26100.253.0

GPU Driver:
- Intel Graphics Driver 31.0.101.2137

Koboldcpp:
- Version: 1.100.1
- Backend: CLBlast (Older CPU)
- GPU Layers: 99
- Threads: 2
- High priority: on
- Keep foreground: on
- ContextShift: on
- FastForward: on
- FlashAttention: off
- KV Cache: F16
- Guidance: on

### Methodology

1. Boot the laptop
2. Wait for 5 minutes to let windows do it's thing
3. Open koboldcpp to the left, task manager to the right in performance tab
4. Open the model config, set backend
5. Run benchmark
6. Save results using notepad and close everything.
