 # spacewallpaper
 create dynamic wallpaper for macOS


- [From @mczachurski/wallpapper](https://github.com/mczachurski/wallpapper/blob/master/README.md) 


### Install 
    brew tap mczachurski/wallpapper
    brew install wallpapper

### Setup
- create wallpapper.json in a folder and add your images together.

### Properties:

- fileName - name of picture file name (you can use same file for few nodes).
- isPrimary - information about image which is primary image (it will be visible after creating heic file). Only one of the file can be primary.
- isForLight - if true picture will be displayed when user chose "Light (static)" wallpaper
- isForDark - if true picture will be displayed when user chose "Dark (static)" wallpaper
- altitude - is the angle between the Sun and the observer's local horizon.
- azimuth - that is the angle of the Sun around the horizon.

### Example

    [
      {
        "fileName": "1.png",
        "isPrimary": true,
        "isForLight": true,
        "altitude": 27.95,
        "azimuth": 279.66
      },
      {
        "fileName": "2.png",
        "altitude": -31.05,
        "azimuth": 4.16
      },
      ...
      {
        "fileName": "16.png",
        "isForDark": true,
        "altitude": -28.63,
        "azimuth": 340.41
      }
    ]
    

### setAsTime 

    [
        {
            "fileName": "1.png",
            "isPrimary": true,
            "isForLight": true,
            "time": "2012-04-23T10:25:43Z"
        },
        {
            "fileName": "2.png",
            "time": "2012-04-23T14:32:12Z"
        },
        {
            "fileName": "3.png",
            "time": "2012-04-23T18:12:01Z"
        },
        {
            "fileName": "4.png",
            "isForDark": true,
            "time": "2012-04-23T20:10:45Z"
        }
    ]

### LightOrDark
    [
        {
            "fileName": "1.png",
            "isPrimary": true,
            "isForLight": true
        },
        {
            "fileName": "2.png",
            "isForDark": true
        }
    ]
    

### Execute command
    wallpapper -i wallpapper.json
    



