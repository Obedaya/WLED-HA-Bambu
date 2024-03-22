# WLED Home Assistant Bambulab Progressbar
This is a tutorial on how to display your Bambulab printing progress on a WLED LED matrix via Home Assistant.  

## Changelog

## Introduction
In Realtime wird der Druckfortschritt auf der LED Matrix dargestellt. Im Vordergrund wird die Uhrzeit und das Datum angezeigt. Die Automation wird automatisch zu Anfang des Druckvorgangs gestartet und 5min nach Ende des Druckvorgangs gestoppt. 

## Installation
### Prerequisites

In order to use it, you first have to install the [Bambulab Integration](https://github.com/greghesp/ha-bambulab)

Note: You also need [HACS](https://hacs.xyz/docs/setup/download/) for the Bambulab Integration

### Installation

Clone the repository:
```bash
git clone https://github.com/Obedaya/WLED-HA-Bambu
```

### WLED
---
First of all you have to add the preset to your WLED LED Matrix.

#### 8 x 32 Matrix
If you have a 8 x 32 big Matrix, it's your lucky day.

If you have no other presets, you can just go to [http://[Your-WLED-IP]/edit](http://[Your-WLED-IP]/edit) and upload presets.json. (ATTENTION: This will override you current presets!)

If you already have presets, download your current presets from [http://[Your-WLED-IP]/edit](http://[Your-WLED-IP]/edit) and append everything from `"2":{...` in presets.json to your downloaded file. 
Note: You probably have to change the id at the beginning, so that you don't have duplicate id's

At the end you file should look something like this:
```json
{"0":{},"1":{"content of preset 1"},"2":{"content of preset 2"}}
```
Then upload the file to [http://[Your-WLED-IP]/edit](http://[Your-WLED-IP]/edit)

#### Different sized Matrix

If you have a different sized Matrix, you have to manualy create the effect. You need 2 overlapping segments. Call one "background" and select the "Percent" effect and set the intensity to 0. Then deselect the segment and create a new one with the name "foreground". For this segment you need to select the "scrolling-text" effect. At this point you can also change the color to your liking.

If you are done, deselect the foreground and select the background and save the preset in its current state.

### Home Assistant
---
Coming soon

## Usage
