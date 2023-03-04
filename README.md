# HomeAssistant
Here is my Home Assistant Lovelace configuration for my tablet dashboard. It supports
- a sidebar to quickly jump to the next pages
- a media-player which plays audio to selectable Spotify connect devices
- a calendar which imports three caldav calendars and shows the next events incl. location and time
- controlling lights and switches via homekit inspired buttons (aligned in a grid) incl. micro-animations and loading
- displaying plant's status
- a shopping list from Todoist which can be filled via Alexa

<img src='https://user-images.githubusercontent.com/67970450/222906231-1b1e67e3-0ad9-4289-b364-f183399f06d1.jpg' width="768" />

## Table of Contents

- [Screenshots](#screenshots)
- [Installation](#installation)
  - [Media-Player](#media-player)
  - [Calendar](#calendar)
  - [Shopping-List](#shopping-list)
- [Inspirations](#inspirations)
- [Todos](#todos)

## Screenshots

| <img src='https://user-images.githubusercontent.com/67970450/222906231-1b1e67e3-0ad9-4289-b364-f183399f06d1.jpg' width="320" /> | <img src="https://user-images.githubusercontent.com/67970450/222906229-bd672da1-b107-4119-ba8a-b133b4a16246.jpg" width="320"> | <img src="https://user-images.githubusercontent.com/67970450/222906238-4b755a26-0930-402e-b299-816de67e0cc2.jpg" width="320"> |
   |:--:| :--: | :--: | 
| *HOME* | *Heizungen* | *Steuerung* |

| <img src='https://user-images.githubusercontent.com/67970450/222906240-162d857e-9dbb-42da-8327-bd59ece54e9a.jpg' width="320" /> | <img src="https://user-images.githubusercontent.com/67970450/222906235-537c0b24-46a8-4bed-bdda-3769e966310a.jpg" width="320">  | <img src="https://user-images.githubusercontent.com/67970450/222906237-0ea01ff9-e41d-47fa-a8d8-6b08bce00551.jpg" width="320"> |
   |:--:| :--: | :--: | 
| *Strom* | *Lichter* | *Pflanzen* |

## Installation

This lovelace UI was created for my tablet and is very customized. Still, some parts can surely be taken over. You will need

- EVERYWHERE: *kiosk-mode* to hide header and sidebar https://github.com/NemesisRE/kiosk-mode
- EVERYWHERE: *card-mod* mainly for CSS styling https://github.com/thomasloven/lovelace-card-mod
- EVERYWHERE: *button-card* which is amazing to create custom buttons https://github.com/custom-cards/button-card
- EVERYWHERE: *sidebar-card* to create a nice sidebar with a clock, weather and menu https://github.com/DBuit/sidebar-card
- HOME: *todoist-card* to display the shopping list created via Alexa https://github.com/grinstantin/todoist-card
- HOME, LICHTER, SCHALTER: *mushroom-cards* for nice buttons and modern UI https://github.com/piitaya/lovelace-mushroom
- HEIZUNGEN: *simple-thermostat-card* to change temperature and see heating modes https://github.com/nervetattoo/simple-thermostat
- HEIZUNGEN: *thermostat-dark-card* displays temperature in a nice circle https://github.com/ciotlosm/lovelace-thermostat-dark-card
- STROM: *mini-graph-card* creates an energy graph on the switch buttons https://github.com/kalkih/mini-graph-card
- LICHTER, SCHALTER: *auto-entities* which helps to autopopulate cards https://github.com/thomasloven/lovelace-auto-entities
- LICHTER: *hue-icons* for nicer looking hue icons https://github.com/arallsopp/hass-hue-icons
- PFLANZEN: *flower-card* for plants https://github.com/Olen/lovelace-flower-card
  - uses *plant* which creates a plant entity in HA https://github.com/Olen/homeassistant-plant

### Media-Player

- To enable the media-player used in my HOME page you will need
  - *mushroom-cards* for the play+pause+skip buttons and artist+song title
  - *mini-media-player* for the progress bar
  - *spotcast* to start playback on Spotify connect devices, e.g. Amazon Show

### Calendar

- To create the calendar used in my HOME page you will need
  - *HASS Calendar Addon* will read google or caldav calendars in a parsable entity https://github.com/kdw2060/hassio-addons/tree/master/hass-addon-calendar
  - Setup the addon and configure your new calendars
  - *button-card* is used to create the calendar UI

### Shopping-List

I am using Todoist to synchronize items from Alexa's shopping list to home assistant.
1. Create a Todoist account https://todoist.com/
2. Install the Todoist skill to your Alexa
3. Install the Todoist card to HA https://github.com/grinstantin/todoist-card

## Inspirations

- Zorrt's dashboard
  - https://www.reddit.com/r/homeassistant/comments/tbjel8/my_dashboard_still_a_work_in_progress_most_prob/
  - https://github.com/zorrt/hass-lovelace


- Mattias Perrson's dashboard
  - https://community.home-assistant.io/t/a-different-take-on-designing-a-lovelace-ui/162594
  - https://github.com/matt8707/hass-config


## Todos

- Use decluttering card to simplify the lovelace-UI
- Use the colors defined by the theme instead of hard-coded colors
- Enhance the design of the shopping list card
- Fix the 20s UI-delay when changing sources via the media-player

