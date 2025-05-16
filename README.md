# SmolVLM real-time camera demo

![demo](./demo.png)

This repository is a simple demo for how to use llama.cpp server with SmolVLM 500M to get real-time object detection

## How to setup

1. Install [llama.cpp](https://github.com/ggml-org/llama.cpp)
2. Run `llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF`  
   Note: you may need to add `-ngl 99` to enable GPU (if you are using NVidia/AMD/Intel GPU)  
   Note (2): You can also try other models [here](https://github.com/ggml-org/llama.cpp/blob/master/docs/multimodal.md)
3. Open `index.html`
4. Optionally change the instruction (for example, make it returns JSON)
5. Click on "Start" and enjoy

## Performance notes

Using cmd: llama-server -m SmolVLM-500M-Instruct-Q8_0.gguf --mmproj mmproj-SmolVLM-500M-Instruct-Q8_0.gguf

`-ngl 99` didn't change much on my 3 yo laptop

Smaller quant SmolVLM-500M-Instruct.Q4_K_M didn't change much in processing time, but this due to using the same mmproj file

Using cmd: llama-server -m SmolVLM-500M-Instruct-f16.gguf --mmproj mmproj-SmolVLM-500M-Instruct-f16.gguf is only 10% slower

