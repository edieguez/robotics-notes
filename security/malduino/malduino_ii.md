# [Malduino II](https://docs.maltronics.com/devices/malduino-2)

## Modes

1. Run `1.txt` script
2. Run `2.txt` script
3. Setup mode

## Setup mode

While in `setup mode` you can edit the `preferences.json` file

> ==You can generate a new preferences file by deleting your current one, and replugging the device==

| Setting          | Default value | Description                                                                    |
|------------------|---------------|--------------------------------------------------------------------------------|
| enable_msc       | false         | Enable USB mass storage (USB drive) in attack mode                             |
| enable_hid       | true          | Enable HID in setup mode                                                       |
| hid1_vid         | 16D0          | (script 1) USB Keyboard Vendor ID                                              |
| hid1_pid         | 103F          | (script 1) USB Keyboard Product ID                                             |
| hid2_vid         | 16D0          | (script 2) USB Keyboard Vendor ID                                              |
| hid2_pid         | 103F          | (script 2) USB Keyboard Product ID                                             |
| hid_rev          | 0100          | USB Keyboard Product Revision                                                  |
| msc_vid          | Maltrncs      | USB Mass Storage Vendor ID                                                     |
| msc_pid          | MalDuino      | USB Mass Storage Product ID                                                    |
| msc_rev          | 1.0           | USB Mass Storage Product Revision                                              |
| default_layout   | US            | Default Keyboard Layout                                                        |
| default_delay    | 5             | Default delay between each line                                                |
| disable_capslock | true          | Turn off capslock before starting attack                                       |
| run_on_indicator | false         | Start script when the user presses capslock, numlock, or another indicator key |
| initial_delay    | 1000          | Startup delay                                                                  |
