# Waywordle
Fun lil wordle game to play inside waywall

## Setup (Manual)
1. Clone to Waywall config folder
```bash
git clone https://github.com/arjuncgore/waywordle.git ~/.config/waywall/waywordle
```
2. Setup in Waywall config
```lua
-- rest of config
local waywordle_cfg = {
    x = 200,
    y = 200,
    size = 7,
    start_key = "F7",
    colors = {
        text = "#FFFFFF",
        incorrect = "#3a3a3c",
        partial = "#f5793a",
        correct = "#85c0f9",
    }
}

require("waywordle.init").setup(config, waywordle_cfg)

return config
```

## Setup (plug.waywall)
```lua
return {
    url = "https://github.com/arjuncgore/waywordle",
    config = function(config)
        require("waywordle.init").setup(config, {
            x = 200,
            y = 200,
            size = 7,
            start_key = "F7",
            colors = {
                text = "#FFFFFF",
                incorrect = "#3a3a3c",
                partial = "#f5793a",
                correct = "#85c0f9",
            }
        })
    end,
    name = "waywordle",
    update_on_load = false,
}
```

## How to play
Press the start/stop key (F7 by default). This will allow you to type your words. You can use backspace to fix mistakes and enter to submit a word.

> Important: Your keyboard will not work while playing, and the only way to get back functionality of your keyboard is to press the start/stop key again.

## Credits
- Lincoln and Justin for the idea
- Alice for motivation
- Woof for solving my biggest headache for this project
