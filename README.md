# Small LLM Tests

For laughs and giggles I wanted to see how "well" my super weak laptop without
dGPU nor AVX/AVX2 support can run LLMs.

## Results

**Model Family**             | **Params** | **Processing Time** | **Processing Speed** | **Generation Time** | **Generation Speed** | **Total Time**
---------------------------- | ---------- | ------------------- | -------------------- | ------------------- | -------------------- | --------------
AceInstruct                  | 1.5B       | 1117.239s           | 7.24T/s              | 179.753s            | 0.56T/s              | 1296.992s
Deepseek R1 Distill Qwen     | 1.5B       | 1168.520s           | 6.92T/s              | 184.623s            | 0.54T/s              | 1353.143s
MobileLLM R1                 | 360M       | 93.758s             | 42.62T/s             | 62.756s             | 1.59T/s              | 156.514s
MobileLLM R1                 | 950M       | 320.887s            | 12.45T/s             | 143.070s            | 0.70T/s              | 463.957s
Falcon 3                     | 1B         | 864.889s            | 9.36T/s              | 148.107s            | 0.68T/s              | 1012.996s
Falcon 3                     | 3B         | 1803.937s           | 4.49T/s              | 315.585s            | 0.32T/s              | 2119.522s
Falcon H1                    | 0.5B       | 661.565s            | 12.23T/s             | 131.768s            | 0.76T/s              | 793.333s
Falcon H1                    | 1.5B       | 1463.552s           | 5.53T/s              | 172.069s            | 0.58T/s              | 1635.621s
Falcon H1                    | 3B         | 3170.326s           | 2.55T/s              | 313.260s            | 0.32T/s              | 3483.586s
Gemma 2                      | 2B         | 2176.875s           | 3.72T/s              | 270.906s            | 0.37T/s              | 2447.781s
Gemma 3                      | 270M       | 174.386s            | 46.40T/s             | 97.553s             | 1.03T/s              | 271.939s
Gemma 3                      | 1B         | 2630.358s           | 3.08T/s              | 125.694s            | 0.80T/s              | 2756.052s
Gemma 3                      | 4B         | 2294.481s           | 3.53T/s              | 401.239s            | 0.25T/s              | 2695.720s
GPT 2                        | 355M       | 34.618s             | 26.69T/s             | 44.871s             | 2.23T/s              | 79.489s
GPT 2                        | 774M       | 95.001s             | 9.73T/s              | 83.584s             | 1.20T/s              | 178.585s
GPT 2                        | 1.5B       | 185.614s            | 4.98T/s              | 137.003s            | 0.73T/s              | 322.617s
Granite 3.1                  | 1B A400M   | 5345.690s           | 1.51T/s              | 178.572s            | 0.56T/s              | 5524.262s

## Models

### Tested

For each model I use different context sizes. See Models table.

**Model Family**             | **Type** | **Params** | **Quants** | **Context** | **Link**
---------------------------- | -------- | ---------- | ---------- | ----------- | --------
AceInstruct                  | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/AceInstruct-1.5B-GGUF?show_file_info=AceInstruct-1.5B.Q8_0.gguf)
Deepseek R1 Distill Qwen     | Hybrid   | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/DeepSeek-R1-Distill-Qwen-1.5B-GGUF?show_file_info=DeepSeek-R1-Distill-Qwen-1.5B-Q8_0.gguf)
MobileLLM R1                 | Instruct | 360M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-360M-GGUF?show_file_info=facebook.MobileLLM-R1-360M.f16.gguf)    
MobileLLM R1                 | Instruct | 950M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-950M-GGUF?show_file_info=facebook.MobileLLM-R1-950M.f16.gguf)
Falcon 3                     | Instruct | 1B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-1B-Instruct-GGUF?show_file_info=Falcon3-1B-Instruct.Q8_0.gguf)
Falcon 3                     | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-3B-Instruct-GGUF?show_file_info=Falcon3-3B-Instruct.Q4_K_M.gguf)
Falcon H1                    | Instruct | 0.5B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-0.5B-Instruct-GGUF?show_file_info=Falcon-H1-0.5B-Instruct-BF16.gguf)
Falcon H1                    | Instruct | 1.5B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-1.5B-Instruct-GGUF?show_file_info=Falcon-H1-1.5B-Instruct-Q8_0.gguf)
Falcon H1                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-3B-Instruct-GGUF?show_file_info=Falcon-H1-3B-Instruct-Q4_K_M.gguf)
Gemma 2                      | Instruct | 2B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/gemma-2-2b-it-GGUF?show_file_info=gemma-2-2b-it.Q8_0.gguf)
Gemma 3                      | Instruct | 270M       | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-270m-it-GGUF?show_file_info=gemma-3-270m-it-F16.gguf)
Gemma 3                      | Instruct | 1B         | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-1b-it-GGUF?show_file_info=gemma-3-1b-it-BF16.gguf)
Gemma 3                      | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3-4b-it-GGUF?show_file_info=gemma-3-4b-it-Q4_K_M.gguf)
Gemma 3n                     | Instruct | 2B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3n-E2B-it-GGUF?show_file_info=gemma-3n-E2B-it-Q4_K_M.gguf)
GPT 2                        | Instruct | 355M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-medium-GGUF?show_file_info=gpt2-medium.f16.gguf)
GPT 2                        | Instruct | 774M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-large-GGUF?show_file_info=gpt2-large.f16.gguf)
GPT 2                        | Instruct | 1.5B       | Q8_0       | 1024        | [link](https://huggingface.co/mradermacher/gpt2-xl-GGUF?show_file_info=gpt2-xl.Q8_0.gguf)
Granite 3.1                  | Instruct | 1B A400M   | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-1b-a400m-instruct-GGUF?show_file_info=granite-3.1-1b-a400m-instruct.f16.gguf)

### To test

**Model**                    | **Type** | **Params** | **Quants** | **Context** | **Link**
-----------------------------| -------- | ---------- | ---------- | ----------- | --------
Granite 3.1                  | Instruct | 3B A800M   | Q4_K_M     | 8192        | [link](https://huggingface.co/DevQuasar/ibm-granite.granite-3.1-3b-a800m-instruct-GGUF?show_file_info=ibm-granite.granite-3.1-3b-a800m-instruct.Q4_K_M.gguf)
Granite 3.1                  | Instruct | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-2b-instruct-GGUF?show_file_info=granite-3.1-2b-instruct.Q8_0.gguf)
Granite 3.1                  | Hybrid   | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.2-2b-instruct-GGUF?show_file_info=granite-3.2-2b-instruct.Q8_0.gguf)
Granite 4.0                  | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-micro-GGUF?show_file_info=granite-4.0-micro-Q4_K_M.gguf)
Granite 4.0 H                | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-h-micro-GGUF?show_file_info=granite-4.0-h-micro-Q4_K_M.gguf)
Llama 3.1 Nemotron Nano v1.1 | Hybrid   | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Llama-3.1-Nemotron-Nano-4B-v1.1-GGUF?show_file_info=Llama-3.1-Nemotron-Nano-4B-v1.1.Q4_K_M.gguf)
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
SmolLM 3                     | Hybrid   | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/SmolLM3-3B-GGUF?show_file_info=SmolLM3-3B-Q4_K_M.gguf)
TinyLlama v1.1               | Instruct | 1.1B       | F16        | 2048        | [link](https://huggingface.co/mradermacher/TinyLlama_v1.1-GGUF?show_file_info=TinyLlama_v1.1.f16.gguf)

To download:

- https://huggingface.co/unsloth/granite-4.0-350m-GGUF?show_file_info=granite-4.0-350m-BF16.gguf
- https://huggingface.co/unsloth/granite-4.0-1b-GGUF?show_file_info=granite-4.0-1b-Q8_0.gguf
- https://huggingface.co/unsloth/granite-4.0-h-350m-GGUF?show_file_info=granite-4.0-h-350m-BF16.gguf
- https://huggingface.co/unsloth/granite-4.0-h-1b-GGUF?show_file_info=granite-4.0-h-1b-Q8_0.gguf
- https://huggingface.co/unsloth/LFM2-350M-GGUF?show_file_info=LFM2-350M-F16.gguf
- https://huggingface.co/unsloth/LFM2-700M-GGUF?show_file_info=LFM2-700M-F16.gguf
- https://huggingface.co/unsloth/LFM2-1.2B-GGUF?show_file_info=LFM2-1.2B-F16.gguf
- https://huggingface.co/mradermacher/LFM2-2.6B-GGUF?show_file_info=LFM2-2.6B.Q8_0.gguf
- https://huggingface.co/mradermacher/LFM2-VL-450M-GGUF?show_file_info=LFM2-VL-450M.f16.gguf
- https://huggingface.co/mradermacher/LFM2-VL-1.6B-GGUF?show_file_info=LFM2-VL-1.6B.f16.gguf
- https://huggingface.co/mradermacher/OpenELM-270M-Instruct-GGUF?show_file_info=OpenELM-270M-Instruct.f16.gguf
- https://huggingface.co/mradermacher/OpenELM-450M-Instruct-GGUF?show_file_info=OpenELM-450M-Instruct.f16.gguf
- https://huggingface.co/mradermacher/OpenELM-1_1B-Instruct-GGUF?show_file_info=OpenELM-1_1B-Instruct.f16.gguf
- https://huggingface.co/mradermacher/OpenELM-3B-Instruct-GGUF?show_file_info=OpenELM-3B-Instruct.Q4_K_M.gguf

Interesting models without GUFFs from preferred providers:

- https://huggingface.co/facebook/MobileLLM-Pro
- https://huggingface.co/FreedomIntelligence/openPangu-Embedded-1B
- https://huggingface.co/LiquidAI/LFM2-VL-3B
- https://huggingface.co/nvidia/Nemotron-H-4B-Instruct-128K

## Testing environment

### Hardware

- Device: ASUS Vivobook E210MA
- CPU: Intel N5000
- GPU: Intel UHD 605
- RAM: 8GB DDR4 2400MHz (single-channel, soldered)
- SSD: Intel 660P 512GB

It's always connected to charger while running benchmarks.

### Software

Windows:
- Edition: Windows 11 IoT Enterprise LTSC
- Version: 24H2
- OS build: 26100.6899
- Experience: Windows Feature Experience Pack 1000.26100.253.0
- Power profile: Performance

GPU Driver:
- Intel Graphics Driver 31.0.101.2137
- Power profile: Performance

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

Notes: 
- No other software is installed on the machine
- Windows defender is not actively running
- Airplane mode on
- Wifi/bluetooth off

### Model selection

Only models that fit inside 5.3GB RAM (7.8GB total, windows taking 2.5GB)
and are available for download on [HuggingFace](https://huggingface.co) as
GUFF are allowed.

I limit myself to the following GUFF authors (in order of preference):

1. unsloth
2. mradermacher
3. DevQuasar

If supported context size is larger than 8192, I use 8192. If lower, I use that
value.

### Methodology

1. Boot the laptop
2. Wait for 5 minutes to let windows do it's thing
3. Open koboldcpp to the left, task manager to the right in performance tab
4. Open the model config, set backend
5. Run benchmark
6. Save results using notepad and close everything.

### Limitations

Due to the amount of time required to run each model, I am only able to do one
run per model.
