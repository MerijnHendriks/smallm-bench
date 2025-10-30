# Small LLM Tests

For laughs and giggles I wanted to see how "well" my super weak laptop without
dGPU nor AVX/AVX2 support can run LLMs. I only look for speed, not output
quality (yet).

## Results

**Model**                    | **Params** | **Processing Time** | **Processing Speed** | **Generation Time** | **Generation Speed** | **Total Time**
---------------------------- | ---------- | ------------------- | -------------------- | ------------------- | -------------------- | --------------
AceInstruct                  | 1.5B       | 1117.239s           | 7.24T/s              | 179.753s            | 0.56T/s              | 1296.992s
Deepseek R1 Distill Qwen     | 1.5B       | 1168.520s           | 6.92T/s              | 184.623s            | 0.54T/s              | 1353.143s
Falcon 3                     | 1B         | 864.889s            | 9.36T/s              | 148.107s            | 0.68T/s              | 1012.996s
Falcon 3                     | 3B         | 1803.937s           | 4.49T/s              | 315.585s            | 0.32T/s              | 2119.522s
Falcon H1                    | 0.5B       | 661.565s            | 12.23T/s             | 131.768s            | 0.76T/s              | 793.333s
Falcon H1                    | 1.5B       | 1463.552s           | 5.53T/s              | 172.069s            | 0.58T/s              | 1635.621s
Falcon H1 (Deep)             | 1.5B       | -                   | -                    | -                   | -                    | -
Falcon H1                    | 3B         | 3170.326s           | 2.55T/s              | 313.260s            | 0.32T/s              | 3483.586s
Gemma 2                      | 2B         | 2176.875s           | 3.72T/s              | 270.906s            | 0.37T/s              | 2447.781s
Gemma 3                      | 270M       | 174.386s            | 46.40T/s             | 97.553s             | 1.03T/s              | 271.939s
Gemma 3                      | 1B         | 2630.358s           | 3.08T/s              | 125.694s            | 0.80T/s              | 2756.052s
Gemma 3                      | 4B         | 2294.481s           | 3.53T/s              | 401.239s            | 0.25T/s              | 2695.720s
Gemma 3n                     | 2B         | 1884.329s           | 4.29T/s              | 374.232s            | 0.27T/s              | 2258.561s
GPT 2                        | 355M       | 34.618s             | 26.69T/s             | 44.871s             | 2.23T/s              | 79.489s
GPT 2                        | 774M       | 95.001s             | 9.73T/s              | 83.584s             | 1.20T/s              | 178.585s
GPT 2                        | 1.5B       | 185.614s            | 4.98T/s              | 137.003s            | 0.73T/s              | 322.617s
Granite 3.1                  | 1B A400M   | 5345.690s           | 1.51T/s              | 178.572s            | 0.56T/s              | 5524.262s
Granite 3.1                  | 3B A800M   | 8248.371s           | 0.98T/s              | 282.961s            | 0.35T/s              | 8531.332s
Granite 3.1                  | 2B         | 3062.854s           | 2.64T/s              | 406.325s            | 0.25T/s              | 3469.179s
Granite 3.2                  | 2B         | 2886.372s           | 2.80T/s              | 407.316s            | 0.25T/s              | 3293.688s
Granite 4.0                  | 350M       | 1297.645s           | 6.24T/s              | 85.256s             | 1.17T/s              | 1382.901s
Granite 4.0                  | 1B         | 1638.892s           | 4.94T/s              | 300.521s            | 0.33T/s              | 1939.413s
Granite 4.0                  | 3B         | 3926.248s           | 2.06T/s              | 454.000s            | 0.22T/s              | 4380.248s
Granite 4.0 H                | 350M       | 1081.546s           | 7.48T/s              | 28.754s             | 3.48T/s              | 1110.300s
Granite 4.0 H                | 1B         | 1372.350s           | 5.90T/s              | 126.103s            | 0.79T/s              | 1498.453s
Granite 4.0 H                | 3B         | 2463.861s           | 3.28T/s              | 221.215s            | 0.45T/s              | 2685.076s
LFM2                         | 350M       | -                   | -                    | -                   | -                    | -
LFM2                         | 700M       | -                   | -                    | -                   | -                    | -
LFM2                         | 1.2B       | -                   | -                    | -                   | -                    | -
LFM2                         | 2.6B       | -                   | -                    | -                   | -                    | -
LFM2 VL                      | 450M       | -                   | -                    | -                   | -                    | -
LFM2 VL                      | 1.6B       | -                   | -                    | -                   | -                    | -
Llama 3.1 Nemotron Nano v1.1 | 4B         | -                   | -                    | -                   | -                    | -
Llama 3.2                    | 1B         | -                   | -                    | -                   | -                    | -
Llama 3.2                    | 3B         | -                   | -                    | -                   | -                    | -
Ministral                    | 3B         | -                   | -                    | -                   | -                    | -
MobileLLM R1                 | 360M       | 93.758s             | 42.62T/s             | 62.756s             | 1.59T/s              | 156.514s
MobileLLM R1                 | 950M       | 320.887s            | 12.45T/s             | 143.070s            | 0.70T/s              | 463.957s
OLMo (0724)                  | 1B         | -                   | -                    | -                   | -                    | -
OLMo 2 (0425)                | 1B         | -                   | -                    | -                   | -                    | -
OpenELM                      | 270M       | -                   | -                    | -                   | -                    | -
OpenELM                      | 450M       | -                   | -                    | -                   | -                    | -
OpenELM                      | 1.1B       | -                   | -                    | -                   | -                    | -
OpenELM                      | 3B         | -                   | -                    | -                   | -                    | -
Phi 3.5 Mini                 | 4B         | -                   | -                    | -                   | -                    | -
Phi 4 Mini                   | 4B         | -                   | -                    | -                   | -                    | -
Phi 4 Mini                   | 4B         | -                   | -                    | -                   | -                    | -
Qwen 2.5                     | 0.5B       | 515.112s            | 15.71T/s             | 124.166s            | 0.81T/s              | 639.278s
Qwen 2.5                     | 1.5B       | -                   | -                    | -                   | -                    | -
Qwen 2.5                     | 3B         | -                   | -                    | -                   | -                    | -
Qwen 2.5 VL                  | 3B         | -                   | -                    | -                   | -                    | -
Qwen 2.5 Omni                | 3B         | -                   | -                    | -                   | -                    | -
Qwen 3                       | 0.6B       | 1964.106s           | 4.12T/s              | 170.627s            | 0.59T/s              | 2134.733s
Qwen 3                       | 1.7B       | 1475.755s           | 5.48T/s              | 242.844s            | 0.41T/s              | 1718.599s
Qwen 3 (2507, instruct)      | 4B         | 3693.251s           | 2.19T/s              | 504.004s            | 0.20T/s              | 4197.255s
Qwen 3 (2507, thinking)      | 4B         | -                   | -                    | -                   | -                    | -
SmallThinker                 | 4B A0.6B   | -                   | -                    | -                   | -                    | -
SmolLM 2                     | 360M       | -                   | -                    | -                   | -                    | -
SmolLM 2                     | 1.7B       | -                   | -                    | -                   | -                    | -
SmolLM 3                     | 3B         | -                   | -                    | -                   | -                    | -
TinyLlama v1.1               | 1.1B       | -                   | -                    | -                   | -                    | -

Some observations not visible in the tests:

- Mamba architectures are indeed better at memory usage, Granite 4.0 H 350M
  took ~500MB less memory to run.
- Smaller models (less than 2B) don't utilize the iGPU 100% all the time during
  processing, making it more energy efficient to run.
- Modern models like Gemma 3 and Granite 4 have constant 0-100% spikes in iGPU
  utilizations, whereas Qwen 2.5 and MobileLLM R1 remain more steady (~50-85%).

## Models

Only models that fit inside 5.3GB RAM (7.8GB total, windows taking 2.5GB), have
270M or more params, are available for download on
[HuggingFace](https://huggingface.co) as GUFF are allowed.

I limit myself to the following GUFF authors (in order of preference):

1. unsloth
2. mradermacher
3. DevQuasar

If supported context size is larger than 8192, I use 8192. If lower, I use that
value. See the `Context` row for the context I use during benchmarking. I don't
load mmproj files if the model has vision support.

**Organization** | **Model**                    | **Type** | **Params** | **Quants** | **Context** | **GUFF**
---------------- | ---------------------------- | -------- | ---------- | ---------- | ----------- | --------
NVIDIA           | AceInstruct                  | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/AceInstruct-1.5B-GGUF?show_file_info=AceInstruct-1.5B.Q8_0.gguf)
Deepseek         | Deepseek R1 Distill Qwen     | Hybrid   | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/DeepSeek-R1-Distill-Qwen-1.5B-GGUF?show_file_info=DeepSeek-R1-Distill-Qwen-1.5B-Q8_0.gguf)
Meta             | MobileLLM R1                 | Instruct | 360M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-360M-GGUF?show_file_info=facebook.MobileLLM-R1-360M.f16.gguf)    
Meta             | MobileLLM R1                 | Instruct | 950M       | F16        | 4096        | [link](https://huggingface.co/DevQuasar/facebook.MobileLLM-R1-950M-GGUF?show_file_info=facebook.MobileLLM-R1-950M.f16.gguf)
Tiiuae           | Falcon 3                     | Instruct | 1B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-1B-Instruct-GGUF?show_file_info=Falcon3-1B-Instruct.Q8_0.gguf)
Tiiuae           | Falcon 3                     | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Falcon3-3B-Instruct-GGUF?show_file_info=Falcon3-3B-Instruct.Q4_K_M.gguf)
Tiiuae           | Falcon H1                    | Instruct | 0.5B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-0.5B-Instruct-GGUF?show_file_info=Falcon-H1-0.5B-Instruct-BF16.gguf)
Tiiuae           | Falcon H1                    | Instruct | 1.5B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-1.5B-Instruct-GGUF?show_file_info=Falcon-H1-1.5B-Instruct-Q8_0.gguf)
Tiiuae           | Falcon H1 (Deep)             | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-1.5B-Deep-Instruct-GGUF?show_file_info=Falcon-H1-1.5B-Deep-Instruct-Q8_0.gguf)
Tiiuae           | Falcon H1                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Falcon-H1-3B-Instruct-GGUF?show_file_info=Falcon-H1-3B-Instruct-Q4_K_M.gguf)
Google           | Gemma 2                      | Instruct | 2B         | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/gemma-2-2b-it-GGUF?show_file_info=gemma-2-2b-it.Q8_0.gguf)
Google           | Gemma 3                      | Instruct | 270M       | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-270m-it-GGUF?show_file_info=gemma-3-270m-it-F16.gguf)
Google           | Gemma 3                      | Instruct | 1B         | BF16       | 8192        | [link](https://huggingface.co/unsloth/gemma-3-1b-it-GGUF?show_file_info=gemma-3-1b-it-BF16.gguf)
Google           | Gemma 3                      | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3-4b-it-GGUF?show_file_info=gemma-3-4b-it-Q4_K_M.gguf)
Google           | Gemma 3n                     | Instruct | 2B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/gemma-3n-E2B-it-GGUF?show_file_info=gemma-3n-E2B-it-Q4_K_M.gguf)
OpenAI           | GPT 2                        | Instruct | 355M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-medium-GGUF?show_file_info=gpt2-medium.f16.gguf)
OpenAI           | GPT 2                        | Instruct | 774M       | F16        | 1024        | [link](https://huggingface.co/mradermacher/gpt2-large-GGUF?show_file_info=gpt2-large.f16.gguf)
OpenAI           | GPT 2                        | Instruct | 1.5B       | Q8_0       | 1024        | [link](https://huggingface.co/mradermacher/gpt2-xl-GGUF?show_file_info=gpt2-xl.Q8_0.gguf)
IBM              | Granite 3.1                  | Instruct | 1B A400M   | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-1b-a400m-instruct-GGUF?show_file_info=granite-3.1-1b-a400m-instruct.f16.gguf)
IBM              | Granite 3.1                  | Instruct | 3B A800M   | Q4_K_M     | 8192        | [link](https://huggingface.co/DevQuasar/ibm-granite.granite-3.1-3b-a800m-instruct-GGUF?show_file_info=ibm-granite.granite-3.1-3b-a800m-instruct.Q4_K_M.gguf)
IBM              | Granite 3.1                  | Instruct | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.1-2b-instruct-GGUF?show_file_info=granite-3.1-2b-instruct.Q8_0.gguf)
IBM              | Granite 3.2                  | Hybrid   | 2B         | F16        | 8192        | [link](https://huggingface.co/mradermacher/granite-3.2-2b-instruct-GGUF?show_file_info=granite-3.2-2b-instruct.Q8_0.gguf)
IBM              | Granite 4.0                  | Instruct | 350M       | BF16       | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-350m-GGUF?show_file_info=granite-4.0-350m-BF16.gguf)
IBM              | Granite 4.0                  | Instruct | 1B         | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-1b-GGUF?show_file_info=granite-4.0-1b-Q8_0.gguf)
IBM              | Granite 4.0                  | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-micro-GGUF?show_file_info=granite-4.0-micro-Q4_K_M.gguf)
IBM              | Granite 4.0 H                | Instruct | 350M       | BF16       | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-h-350m-GGUF?show_file_info=granite-4.0-h-350m-BF16.gguf)
IBM              | Granite 4.0 H                | Instruct | 1B         | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-h-1b-GGUF?show_file_info=granite-4.0-h-1b-Q8_0.gguf)
IBM              | Granite 4.0 H                | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/granite-4.0-h-micro-GGUF?show_file_info=granite-4.0-h-micro-Q4_K_M.gguf)
Liquid AI        | LFM2                         | Instruct | 350M       | F16        | 8192        | [link](https://huggingface.co/unsloth/LFM2-350M-GGUF?show_file_info=LFM2-350M-F16.gguf)
Liquid AI        | LFM2                         | Instruct | 700M       | F16        | 8192        | [link](https://huggingface.co/unsloth/LFM2-700M-GGUF?show_file_info=LFM2-700M-F16.gguf)
Liquid AI        | LFM2                         | Instruct | 1.2B       | F16        | 8192        | [link](https://huggingface.co/unsloth/LFM2-1.2B-GGUF?show_file_info=LFM2-1.2B-F16.gguf)
Liquid AI        | LFM2                         | Instruct | 2.6B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/LFM2-2.6B-GGUF?show_file_info=LFM2-2.6B.Q8_0.gguf)
Liquid AI        | LFM2 VL                      | Instruct | 450M       | F16        | 8192        | [link](https://huggingface.co/mradermacher/LFM2-VL-450M-GGUF?show_file_info=LFM2-VL-450M.f16.gguf)
Liquid AI        | LFM2 VL                      | Instruct | 1.6B       | F16        | 8192        | [link](https://huggingface.co/mradermacher/LFM2-VL-1.6B-GGUF?show_file_info=LFM2-VL-1.6B.f16.gguf)
NVIDIA           | Llama 3.1 Nemotron Nano v1.1 | Hybrid   | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Llama-3.1-Nemotron-Nano-4B-v1.1-GGUF?show_file_info=Llama-3.1-Nemotron-Nano-4B-v1.1.Q4_K_M.gguf)
Meta             | Llama 3.2                    | Instruct | 1B         | F16        | 8192        | [link](https://huggingface.co/unsloth/Llama-3.2-1B-Instruct-GGUF?show_file_info=Llama-3.2-1B-Instruct-F16.gguf)
Meta             | Llama 3.2                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Llama-3.2-3B-Instruct-GGUF?show_file_info=Llama-3.2-3B-Instruct-Q4_K_M.gguf)
Ministral        | Ministral                    | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Ministral-3b-instruct-GGUF?show_file_info=Ministral-3b-instruct.Q4_K_M.gguf)
Allen AI         | OLMo (0724)                  | Instruct | 1B         | F16        | 4096        | [link](https://huggingface.co/mradermacher/OLMo-1B-0724-hf-GGUF?show_file_info=OLMo-1B-0724-hf.f16.gguf)
Allen AI         | OLMo 2 (0425)                | Instruct | 1B         | Q8_0       | 4096        | [link](https://huggingface.co/mradermacher/OLMo-2-0425-1B-GGUF?show_file_info=OLMo-2-0425-1B.Q8_0.gguf)
Apple            | OpenELM                      | Instruct | 270M       | F16        | 2048        | [link](https://huggingface.co/mradermacher/OpenELM-270M-Instruct-GGUF?show_file_info=OpenELM-270M-Instruct.f16.gguf)
Apple            | OpenELM                      | Instruct | 450M       | F16        | 2048        | [link](https://huggingface.co/mradermacher/OpenELM-450M-Instruct-GGUF?show_file_info=OpenELM-450M-Instruct.f16.gguf)
Apple            | OpenELM                      | Instruct | 1.1B       | F16        | 2048        | [link](https://huggingface.co/mradermacher/OpenELM-1_1B-Instruct-GGUF?show_file_info=OpenELM-1_1B-Instruct.f16.gguf)
Apple            | OpenELM                      | Instruct | 3B         | Q4_K_M     | 2048        | [link](https://huggingface.co/mradermacher/OpenELM-3B-Instruct-GGUF?show_file_info=OpenELM-3B-Instruct.Q4_K_M.gguf)
Microsoft        | Phi 3.5 Mini                 | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Phi-3.5-mini-instruct-GGUF?show_file_info=Phi-3.5-mini-instruct.Q4_K_M.gguf)
Microsoft        | Phi 4 Mini                   | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Phi-4-mini-instruct-GGUF?show_file_info=Phi-4-mini-instruct-Q4_K_M.gguf)
Microsoft        | Phi 4 Mini                   | Thinking | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Phi-4-mini-reasoning-GGUF?show_file_info=Phi-4-mini-reasoning-Q4_K_M.gguf)
Alibaba Cloud    | Qwen 2.5                     | Instruct | 0.5B       | F16        | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-0.5B-Instruct-GGUF?show_file_info=Qwen2.5-0.5B-Instruct.f16.gguf)
Alibaba Cloud    | Qwen 2.5                     | Instruct | 1.5B       | Q8_0       | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-1.5B-Instruct-GGUF?show_file_info=Qwen2.5-1.5B-Instruct.Q8_0.gguf)
Alibaba Cloud    | Qwen 2.5                     | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-3B-Instruct-GGUF?show_file_info=Qwen2.5-3B-Instruct.Q4_K_M.gguf)
Alibaba Cloud    | Qwen 2.5 VL                  | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/Qwen2.5-VL-3B-Instruct-GGUF?show_file_info=Qwen2.5-VL-3B-Instruct.Q4_K_M.gguf)
Alibaba Cloud    | Qwen 2.5 Omni                | Instruct | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen2.5-Omni-3B-GGUF?show_file_info=Qwen2.5-Omni-3B-Q4_K_M.gguf)
Alibaba Cloud    | Qwen 3                       | Instruct | 0.6B       | BF16       | 8192        | [link](https://huggingface.co/unsloth/Qwen3-0.6B-GGUF?show_file_info=Qwen3-0.6B-BF16.gguf)
Alibaba Cloud    | Qwen 3                       | Instruct | 1.7B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/Qwen3-1.7B-GGUF?show_file_info=Qwen3-1.7B-Q8_0.gguf)
Alibaba Cloud    | Qwen 3 (2507)                | Instruct | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen3-4B-Instruct-2507-GGUF?show_file_info=Qwen3-4B-Instruct-2507-Q4_K_M.gguf)
Alibaba Cloud    | Qwen 3 (2507)                | Thinking | 4B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/Qwen3-4B-Thinking-2507-GGUF?show_file_info=Qwen3-4B-Thinking-2507-Q4_K_M.gguf)
PowerInfer       | SmallThinker                 | Thinking | 4B A0.6B   | Q4_K_M     | 8192        | [link](https://huggingface.co/mradermacher/SmallThinker-4BA0.6B-Instruct-GGUF?show_file_info=SmallThinker-4BA0.6B-Instruct.Q4_K_M.gguf)
HuggingFace      | SmolLM 2                     | Instruct | 360M       | F16        | 8192        | [link](https://huggingface.co/unsloth/SmolLM2-360M-Instruct-GGUF?show_file_info=SmolLM2-360M-Instruct-F16.gguf)
HuggingFace      | SmolLM 2                     | Instruct | 1.7B       | Q8_0       | 8192        | [link](https://huggingface.co/unsloth/SmolLM2-1.7B-Instruct-GGUF?show_file_info=SmolLM2-1.7B-Instruct-Q8_0.gguf)
HuggingFace      | SmolLM 3                     | Hybrid   | 3B         | Q4_K_M     | 8192        | [link](https://huggingface.co/unsloth/SmolLM3-3B-GGUF?show_file_info=SmolLM3-3B-Q4_K_M.gguf)
TinyLlama        | TinyLlama v1.1               | Instruct | 1.1B       | F16        | 2048        | [link](https://huggingface.co/mradermacher/TinyLlama_v1.1-GGUF?show_file_info=TinyLlama_v1.1.f16.gguf)

### Excluded

These models need to wait until I benchmarked everything else:

Qwen3 VL (requires koboldcpp support)
- https://huggingface.co/Qwen/Qwen3-VL-2B-Thinking
- https://huggingface.co/Qwen/Qwen3-VL-2B-Instruct
- https://huggingface.co/Qwen/Qwen3-VL-4B-Thinking
- https://huggingface.co/Qwen/Qwen3-VL-4B-Instruct

SmolLM 1
- https://huggingface.co/HuggingFaceTB/SmolLM-360M-Instruct
- https://huggingface.co/HuggingFaceTB/SmolLM-1.7B-Instruct

SmolVLM 1
- https://huggingface.co/HuggingFaceTB/SmolVLM-256M-Instruct
- https://huggingface.co/HuggingFaceTB/SmolVLM-500M-Instruct
- https://huggingface.co/HuggingFaceTB/SmolVLM-Instruct

SmolVLM 2
- https://huggingface.co/HuggingFaceTB/SmolVLM2-256M-Video-Instruct
- https://huggingface.co/HuggingFaceTB/SmolVLM2-500M-Video-Instruct
- https://huggingface.co/HuggingFaceTB/SmolVLM2-2.2B-Instruct

These models are too small to be considered right now, but might check in the
future:

- https://huggingface.co/openai-community/gpt2
- https://huggingface.co/facebook/MobileLLM-R1-140M
- https://huggingface.co/HuggingFaceTB/SmolLM-135M-Instruct
- https://huggingface.co/HuggingFaceTB/SmolLM2-135M-Instruct

These models don't have GUFFs from the preferred providers:

- https://huggingface.co/facebook/MobileLLM-Pro
- https://huggingface.co/FreedomIntelligence/openPangu-Embedded-1B
- https://huggingface.co/LiquidAI/LFM2-VL-3B
- https://huggingface.co/nvidia/Nemotron-H-4B-Instruct-128K
- https://huggingface.co/microsoft/Phi-4-mini-flash-reasoning

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
- Variant: koboldcpp-oldcpu.exe
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

### Methodology

1. Boot the laptop
2. Wait for 5 minutes to let windows do it's thing
3. Open koboldcpp to the left, task manager to the right in performance tab
4. Open the model config, set backend to CLBLast (Older CPU)
5. Run benchmark
6. Save results using notepad and close everything.

### Limitations

Due to the amount of time required to run each model, I am only able run each
model once.
