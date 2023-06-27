# ESP32_JSON_settings
Web-based settings interface for ESP32 projects. Kept simple to save space in flash.

#### Note: This is work in progress, it does not actually work yet!

Written by @chaoticneutralczech with [help from the ArduinoJSON community](https://github.com/bblanchon/ArduinoJson/discussions/1939) (thanks @bblanchon!). Originally written for [my train departure board simulator](https://github.com/ChaoticNeutralCzech/ESP32_Odjezdova_tabule).

### The project will implement:

- [ ] Basic Wi-Fi AP + server functionality
- [ ] A static or dynamic (❓) JSON *thing* (document or object❓) with a fixed number of key-value pairs; those can be booleans, integers or strings: no subobjects or arrays. [Example](https://github.com/ChaoticNeutralCzech/ESP32_JSON_settings/blob/main/example_json.json)
- [ ] On-demand, pre-done or client-side (❓) conversion from the JSON *thing* to a HTML webpage (example: [code](https://github.com/ChaoticNeutralCzech/ESP32_JSON_settings/blob/main/example_html.html)/[page](https://raw.githack.com/ChaoticNeutralCzech/ESP32_JSON_settings/main/example_html.html)) where the user can edit values for each key.
- [ ] Conversion from the HTML webpage's *Submit* action response back to the JSON *thing* that stores the values.
- [ ] Storing the JSON *thing* (serialized or deserialized ❓) in non-volatile memory (vEEPROM or SPIFFS❓) and accessing it when settings are loaded on boot.

Basically, manage the settings of an ESP32 project as a JSON *thing* and present them to the user in a friendly way:  
![Images make websites more appealing so let's screenshot a website and use that! That's how 90 % of the internet works anyway.](https://raw.githubusercontent.com/ChaoticNeutralCzech/ESP32_JSON_settings/main/example_html_render.png)

### Goals outside the minimum viable product

Not going to be implemented right away  but necessary should this ever get a practical release.

- [ ] Turn this into a handy standalone `.hpp` file people can use as a library.
- [ ] Allow export of the settings by letting the client download the JSON file, and import them by allowing uploads of such file. Due to anticipated multiple releases of people's projects using this library, missing/extra key-value pairs will need to be dealt with appropriately. 
