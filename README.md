# mini_pupper_web_controller

Replaces PS4 joystick by a web GUI that can be run on a smartphone

## Installation

The following describes the steps for an installation from scratch that installs all components required.
It also install a pygame based keyborad controller that you might find usefull in certain circumstances

- flash 20220720_v2.0.1_MiniPupper_V1&V2_Controller_Ubuntu_22.04.img to SD card
- on minipupper open a terminal:
- git clone https://github.com/mangdangroboticsclub/minipupper-bsp.git
- git clone -b minipupper https://github.com/mangdangroboticsclub/StanfordQuadruped.git
- git clone https://github.com/mangdangroboticsclub/mini_pupper_web_controller.git

- ./minipupper-bsp/install.sh; sudo reboot
- ./minipupper-bsp/update_kernel_modules.sh; sudo reboot
- cd StanfordQuadruped
- ./install.sh
- ./configure_network.sh <SSID> <PASSWORD>
- cd ~
- ./mini_pupper_web_controller/webserver/install.sh
- sudo apt-get install -y libsdl2-2.0-0
- sudo pip3 install pygame
- git clone https://github.com/stanfordroboticsclub/PupperKeyboardController.git
- sudo reboot

## Run
Point a web browser to http://x.x.x.x:8080 where x.x.x.x is the IP address of your minipupper
