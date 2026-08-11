# opentank
(WORK IN PROGRESS) A smart home sensor hub with ESP32-C6, rich analog capabilities, and full self-powering.
https://youtu.be/-s6jZ4U3TzU

## Important note!!!
The D-/D+ lines at the Type-C connector and SDA/SCL lines for U17 are still swapped!!! If you want to modify this and make changes for your own project, keep this in mind! Otherwise feel free to have a peak around in the PCB layout. Another thing: the templateforconfiguration.yaml (for Home Assistant) is still somewhat broken because the value will never go below 0 with this logic. I'll need to fix this soon. fulldevicecode.yaml is what the PCB gets programmed with, and works flawlessly as far as I've observed (2 months+ runtime so far). I also will be cleaning this up soon though by trying to make some contributions to ESPHome's repo to get rid of the need for so many lambdas. Questions? Email me at rain@haaseindustries.com or comment on my YouTube video.
