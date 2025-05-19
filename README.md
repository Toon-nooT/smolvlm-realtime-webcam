# SmolVLM real-time camera demo

![Screenshot 1](./screenshot1.jpg)
![Screenshot 2](./screenshot2.jpg)

This repository is a simple web based demo for how to use llama.cpp server with SmolVLM 500M. It can describe the scene, in this case, whether the person is asleep. Notable change from the [original repo](https://github.com/ngxson/smolvlm-realtime-webcam) is that the calls are not sent out async anymore.

## How to setup

1. Install [llama.cpp](https://github.com/ggml-org/llama.cpp)
2. Run `llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF`  
   Note: you may need to add `-ngl 99` to enable GPU (if you are using NVidia/AMD/Intel GPU)  
   Note (2): You can also try other models [here](https://github.com/ggml-org/llama.cpp/blob/master/docs/multimodal.md)
3. Open `index.html`
4. Optionally change the instruction (for example, make it returns JSON)
5. Click on "Start" and enjoy

## Performance notes

I used llama-b5415-bin-win-vulkan-x64 on my igp of AMD Ryzen 5 PRO 5650U and this command: llama-server -m SmolVLM2-2.2B-Instruct-Q8_0.gguf --mmproj mmproj-SmolVLM2-2.2B-Instruct-Q8_0.gguf -ngl 99
