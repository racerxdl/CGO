
Commands
======================


To execute a command do a GET request to http://192.168.42.1/cgi-bin/cgi?CMD=**COMMAND**


* **GET_AUDIO_SW** => Get Audio Switch Status (If the audio is enabled or not)
    * Return: 
        * `rval` as resultCode.
        * `audio_sw` as boolean (true if enabled)
* **GET_CAM_MODE** => Gets the camera
    * Return: 
        * `rval` as resultCode
        * `mode` as Camera Mode (To Confirm)
* **GET_STATUS** => Gets the current status (configuration)
    * Return: 
        * `rval` as resultCode
        * `sdfree` as sdcard free space
        * `exposure_value` as exposure value (EV)
        * `iso_value` as ISO value (String: ISO_100)
        * `shutter_time` as shutter time (String: 60)
        * `white_balance` as white balance (String)
        *  `video_mode` as video mode (String: 1920x1080F24)
* **GET_IQ_TYPE** => Gets the HUE (dafuq?)
    * Return: 
        * `rval` as resultCode
        * `IQ_type` as HUE value (String) ("0" for Nature, "1" for Gorgeous", "2" for RAW, "3" for Night)
* **GET_PHOTO_FORMAT** => Gets the Photo Format
    * Return: 
        *  `rval` as resultCode
        *  `photo_format` as photo format (String: jpg)
* **GET_VIDEO_MODE** => Gets video mode
    * Return:
        *  `rval` as resultCode
        *  `video_mode` as Video Mode (String 4096x2160F24)
* **GET_SPACE_FREE** => Gets SDCard Free Space
    * Return: 
        *  `rval` as resultCode
        *  `param` as free space (Double)
* **GET_FW_VERSION** => Gets Camera Firmware Version
    * Return 
        *  `rval` as resultCode
        *  `model` as Camera model (String)
        *  `YUNEEC_ver` as Firmware Version
* **FORMAT_CARD** =>  Formats the SDCard
    * Return: `rval` as resultCode.
* **INDEX_PAGE** => Initializes the Camera
    * Return 
        *  `rval` as resultCode
        *  `iq_type` as HUE (Optional Int)
        *  `white_balance` as WhiteBalance Mode (Optional String)
        *  `exposure_value` as EV (Optional String)
        *  `sharpness` as Sharpness (Optional Int)
        *  `sdfree` as Free SD Card Space (Optional String)
        *  `sdtotal` as Total SD Card Size (Optional String)
        *  `video_mode` as Video Mode (Optional String)
        *  `speed_rate` as ??Speed Rate?? (Optional String)
        *  `fw_ver` as Firmware Version (Optional String)
        *  `cam_mode` as Camera Mode (Optional String)
        *  `status` as Camera Status (Optional String, only if cam_mode == 1 [ recording ])
        *  `record_time` as Current Recording Status (Optional String, only if cam_mode == 1 [ recording ])
        *  `ae_enable` as Auto Exposure Enabled (Optional String)
        *  `shutter_time` as Shutter Time (Optional String)
        *  `iso_value` as ISO Value (Optional String)
        *  `exposure_value` as EV (Optional String)
* **RESET_DEFAULT** => Reset Camera Defaults
    * Return: 
        *  `rval` as resultCode
* **SET_AUDIO_SW** => Sets Audio Switch (Enable/Disable Sound)
    * Params: 
        *  `mode` as Switch Mode (0 => disabled, 1 => enabled)  
    * Return: 
        *  `rval` as resultCode
* **SET_AE_ENABLE** => Sets AutoExposure Enable
    * Params: 
        *  `mode` as Switch Mode (0 => disabled, 1 => enabled)  
    * Return: 
        *  `rval` as resultCode
* **SET_CAM_MODE** => Sets Camera Mode
    * Params: 
        *  `mode` as Camera Mode (String) ("photo" or "video")
    * Return: 
        *  `rval` as resultCode
* **SET_TIME** => Sets Camera Time
    * Params: 
        *  `time` as Current Time (String) (Format: yyyy-MM-dd_HH:mm:ss)
    * Return: 
        *  `rval` as resultCode
* **SET_EXPOSURE_VALUE** => Sets Camera Exposure Value
    * Params: 
        *  `mode` as EV Value.
    * Return: 
        *  `rval` as resultCode
* **SET_IQ_TYPE** => Sets the HUE
    * Params: 
        *  `mode` as HUE (String) ("0" for Nature, "1" for Gorgeous", "2" for RAW, "3" for Night)
    * Return: 
        *  `rval` as resultCode
* **SET_SH_TM_ISO** => Sets Shutter Time and ISO
    * Params: 
        *  `time` as Shutter Time (String) ("30" for 1/30)
        *  `value` as ISO Value (String) ("100")
    * Return: 
        *  `rval` as resultCode
* **SET_PHOTO_FORMAT** => Sets Photo Format
    * Params: 
        *  `value` as Format (String) ("raw" or "jpg")
    * Return: 
        *  `rval` as resultCode
* **SET_VIDEO_MODE** => Sets Video Mode
    * Params: 
        *  `vidoe_mode` as Video Mode (String) (40964x2160F24) [BTW, its REALLY **vidoe_mode**]
    * Result: 
        *  `rval` as resultCode
* **SET_WHITEBALANCE_MODE** => Sets WhiteBalance
    * Params: 
        *  `mode` as WhiteBalance Mode (Integer) (0 for Auto, 1 for Incandescent, 2 for Sunset, 3 for Sunny, 5 for Cloudy, 6 for Lock WB, 7 for Fluorescent)
    * Result: 
        *  `rval` as resultCode
* **START_RECORD** => Start recording video
    * Result: 
        *  `rval` as resultCode
* **STOP_RECORD** => Stop recording video
    * Result:
        *  `rval` as resutlCode
* **TAKE_PHOTO** => Takes a picture
    * ResultL 
        *  `rval` as resultCode
    