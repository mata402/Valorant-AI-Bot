# Valorant-AI-Bot
A bot that can play Valorant on its own. This is a showcase, code will not be made public to prevent cheating.

![gif](./bot.gif)

- Fully computer vision based thanks to [OpenCV](https://github.com/opencv/opencv-python)
- Real-time object detection with [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5) architecture implemented in PyTorch, accelerated with NVIDIA's CUDA
- No game modifications or memory access
- Undetectable by Riot Vanguard's anti-cheat system

## How it Works

### Aim

- Screenshot centre
- Pass through YOLOv5 image clasification model trained on 2,000 images to find targets
- Validate targets based on colour and find best target
- Calculate mouse input accounting for recoil and smoothing

### Navigation

- Screenshot map
- Edge detection
- Raycasting and mapping
- Determine best route
- Calculate mouse and keyboad input to correct the angle

### Input

- Keyboard inputs are emulated
- Mouse inputs encoded to an arduino leonardo
- Arduino sends mouse input back to the computer as a physical HID to bypass Riot Vanguard's anti-cheat system