# ESPHome Button+ - Music card

## Usage

* Add the music card file to the package files and supply the `entity_id`
    ```
    substitutions:
    music_card_enity_id: 'media_player.media_keuken_2'
    package:
        remote_package_files:
        url: https://github.com/dixi83/ESPHome_ButtonPlus
        files: [<other files>,'package/cards/music.yaml']
    ```
* Add the music card to the main display `lambda` and give it the position you want
    ```
    id(music_card).execute(20, 125);
    ```

* Add the icons buttons to the BAR's

    Select one of the folowing types:
    * `volume_up`
    * `volume_down`
    * `next`
    * `prev`
    * `playpause`
    * `power`
  
    ```
    id(music_card_bar).execute("volume_up");
    ```

* add actions to the buttons
    Select the a matching action for the button:
    * `music_card_vol_up`
    * `music_card_vol_down`
    * `music_card_next`
    * `music_card_prev`
    * `music_card_playpause`
    * `music_card_power`

    ```
    id(music_card_vol_up).execute();
    ```
