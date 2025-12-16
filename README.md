# Home Assistant Holiday Countdown Cards

This repository contains YAML configurations for Home Assistant Lovelace cards that display countdowns to various holidays.

## Installation

1.  **Copy the files:**
    *   Place the `template.yaml` file in your Home Assistant `config` directory.


2.  **Include the template sensors:**
    Add the following line to your `configuration.yaml` file. If you already have a `template:` section, add the `!include` line under it.

    ```yaml
    template: !include template.yaml
    ```

3.  **Restart Home Assistant:**
    Restart your Home Assistant instance to load the new template sensors.

## Card Configuration

Each card is a `custom:button-card`. To use them in your Lovelace dashboard, you can either copy the contents of the card's YAML file into a manual card, or use `!include` to include the card configuration from the file.

### Background Images

The cards use a background image. You can use any image you like.

1.  **Place the image in the `www` directory:**
    Place your desired background image in the `www` directory of your Home Assistant `config` folder. If the `www` directory does not exist, you will need to create it.

2.  **Reference the image in the card configuration:**
    In the card's YAML configuration, the background image is referenced using `/local/`. For example, if you place an image named `Christmas.jpg` in the `www` directory, the path in the card configuration should be `/local/Christmas.jpg`.

    ```yaml
    styles:
      card:
        - background-image: url("/local/Pictures/Christmas.jpg")
    ```

    You will need to update the `background-image` path in each card's configuration to point to the image you have chosen.

## Holiday Videos

*   [Christmas Example](./Holidays/Christmas/Christmas.mov)
