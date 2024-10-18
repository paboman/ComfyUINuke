# comfyUINuke

![Static Badge](https://img.shields.io/badge/Nuke_v12-PASS-green) ![Static Badge](https://img.shields.io/badge/Nuke_v13-PASS-green) ![Static Badge](https://img.shields.io/badge/Nuke_v14-PASS-green) ![Static Badge](https://img.shields.io/badge/Nuke_v15-PASS-green) 
![Static Badge](https://img.shields.io/badge/OSX-green) ![Static Badge](https://img.shields.io/badge/WIN-green) ![Static Badge](https://img.shields.io/badge/Linux-green) 

This fork provides ONLY easier Installation instructions


Use stable diffusion via comfyUI inside Nuke.
Tutorials and proper documentation will follow.


## Requirements

- Nuke 12 or higher
- You need to have a running [ComfyUI](https://github.com/comfyanonymous/ComfyUI) (Standard or Portable)
- [ComfyUI-HQ-Image-Save](https://github.com/spacepxl/ComfyUI-HQ-Image-Save) (required to load images and sequences and work with EXR)

## Installation

1. Download the code

2. Copy the content of the .zip into your .nuke folder: `/Users/youruser/.nuke/`

3. Rename the folder from `ComfyUINuke-main` to `ComfyUINuke`

4. Create a `init.py` file in `/Users/youruser/.nuke/`

5. Edit the created `init.py`, add the following lines and Replace `youruser` to mach your actual username.

```sh
import nuke
nuke.pluginAddPath("/Users/youruser/.nuke/comfyUINuke")
```


## Use

I'm providing 3 basic workflows templates as examples.
Workflows must have a "translation.py" to work inside nuke (check Workflows folder)

1. Open Nuke

2. Press Tab and create `comfyUI_Nuke toolset`

3. Setup the settings tab with your server address and disk folder:

    Default server: `http://127.0.0.1:8188`
    Directory: `/wherever/you/installed/ComfyUI/`

4. Save the toolset with your defaults.


## Demo

<a href="http://www.youtube.com/watch?feature=player_embedded&v=p5Z8fSBkCoo" target="_blank"><img src="http://img.youtube.com/vi/p5Z8fSBkCoo/mqdefault.jpg"
alt="Click to Watch the video" width="240" height="135" border="10" /><br>View the demo on Youtube</a>

## Errors

| Error | Causes |
| --- | --- |
|[Errno 61] Connection Refused | ComfyUI is not running or wrong network address |
|[Http Error 400 or 40X] Bad Request | The workflow .json file has something incompatible on it.<br/>Usually your system has a checkpoint that has another name, ".safetensors" instead of ".ckpt" for example. ComfyUI terminal will tell you which parameter is wrong.<br/>Drag the workflow from the "ComfyUINuke/Workflows" folder into ComfyUI, fix the issue and save the workflow file overwriting the problematic one.<br/>Do not forget to always save the files with  "Save (API format) " (ConfyUI > Settings > Enable Dev mode Options) |
|RuntimeError: /users/youruser/.nuke/comfyUINuke/toolSets/comfyUI_Nuke.nk is for nuke15.0v1; this is nuke14.1v4|Open and Save `comfyUI_Nuke.nk` in whatever Nuke version you use

## Bug report and suggestions

Are welcome, I'm looking for improvement ideas and UI suggestions, new functionalities, etc.
Open to colaboration, submit your commits! Submit issues here on Github.

## To do

A proper workflow translator. Proper documentation and tutorials
Sequence handling

## EXR handling
Check this extension that allows to use exr
https://github.com/spacepxl/ComfyUI-HQ-Image-Save

## Workflows
If you want to get some specific workflow translated inside Nuke, lets talk.

## Coffee
<a href="https://www.paypal.com/paypalme/MBORGO">Love it? Buy me a coffee</a>
