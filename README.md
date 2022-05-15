AutoMatch for OkCupid
=====================

**AutoMatch for OkCupid** is a CLI bot for OkCupid which will (probably) get you better, faster and more reliable interactions.

# About

This software was designed just for fun, playing around with external APIs and as a learning exercise. I won't provide any kind of pro-level support for this software and you shouldn't expect it to work for long, since OkCupid's API could change at any time without prior notice.

For more information about OkCupid's API, please check the `queries` folder at the root of this project.

# Features

- [X] Forbidden strings list

    Create a file named `forbidden_strings` and type the keywords and/or sentences that would make you feel uninterested about a recommendation, strings are separated by newlines.

- [X] Known profiles list

    The script will keep track of known profiles (any profile it's seen throughout it's lifetime on the current device) and automatically give them a "pass" if they've been seen before. This is a workaround for OkCupid's API where it might recommend people you've already liked and they've rejected your like in the past.

- [X] Irrelevant bio blocking

    Detect and automatically skip profiles without a real bio (automatic parsing of bios containing just an Instagram username). Empty bios will also be skipped. 

- [X] Automatic or manual likes

    Toggle `ASK_BEFORE_LIKE` in order to set whether you want the bot to automatically like suggested profiles that match your criteria or get a selection of choices, using the manual mode also allows you to check your suggested match photos by typing "p".

- [X] Customizable settings

    Tweak the algorithm by playing around with the values within the `settings.ini` file. This file will be automatically generated during the first startup. Invalid values will be ignored and their defaults will be loaded instead.

- [ ] ~~Main menu with account settings options (max distance, age range, etc.).~~

# Requirements

- PHP 7.4 or greater
- cURL extension for PHP

# Usage

- Run the program: `php index.php`, you'll be asked for a cookie list. Continue with the next steps to find it.
- Sign into **OkCupid** with your **desktop computer using a web browser**.
- Open **dev tools (hit F12)** and **reload the page**.
- Select the **Network** tab and choose **Fetch/XHR** from the top bar.
- Pick any request from the list, once the **Headers** window has opened, check the **Request URL**. Make sure it starts with "https://www.okcupid.com". If it doesn't, go through the rest until you find one that matches.
- Once you've found it, scroll to the bottom of the **Headers** tab and copy the value of the **cookie** header.
- Paste it in the console and hit enter. That's it, you're good to go!

# Disclaimer

Please take into consideration that I'm not affiliated in any way with the OkCupid company. All this code has been written through experimentation, public documentation found online and reverse engineering of network requests found in the Android app with no intent to cause any damages.

If you feel like this isn't the case, feel free to file a takedown request.

# License

This project is licensed under the terms of [The Unlicense](LICENSE).