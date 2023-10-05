# Fullscreen Clock with Alarm

  A simple fullscreen digital clock built with Python's `tkinter` module. Apart from just telling the time, the clock also has a basic alarm feature.

## Features:

  **4 Versions**:

    V-1.0x: Round clock.

    v-1.1x: Round clock with visual alarm.

    v-1.2x: Round clock with GPIO Buzzer alarm. Customized for Raspberry Pi.

    v-1.3x: Round clock with audio file alarm.

  **Fullscreen Clock**: Display time in a frameless window mode.

  **Interactive**: Click anywhere on the screen to close the application.

  **Set Alarm**: Incremental buttons to set hours and minutes for the alarm.

  **Visual Alarm**: A pop-up notification appears when the alarm rings.

  **Stop/Reset Alarm**: Buttons to stop and keep the previous alarm, or stop and reset the alarm.

## Prerequisites:

  **Python 3.x**

  **tkinter** module (typically comes pre-packaged with Python standard distributions).

## Installation:

  1. **Clone the repository and navigate to the directory**:

  ```
  git clone https://github.com/B-Boone/Alarm_Clock
  cd Alarm_Clock
  ```

  2. **Install dependencies**:

  ```
  pip3 install tkinter
  ```

  3. **Move alarm.wav file to home directory**: Only for V-1.32 (audio version)

  ```
  mv ~/Alarm_Clock/alarm.wav ~
  ```

## How to Use: 

  1. **Run the Application**: Make sure to use the correct version number! Check the version number of the file you want to use, as we are now on version number 1.x1!

    V-1.00
    ```
    python3 clock_V-1.00.py
    ```
  ![2023-09-29-112542_1920x1080_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/4300af78-4376-4d57-8db2-e8a3c194d26f)

    V-1.13
    ```
    python3 clock_V-1.13.py
    ```
  ![2023-10-03-104239_1920x1080_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/6c2c4981-83bd-4ed7-adcf-7ea2d02f100a)

    V-1.23
    ```
    python3 clock_V-1.23.py
    ```
  ![2023-09-29-114654_640x480_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/1a1fb150-cc61-48be-96fe-14b0fbe9dc59)

    V-1.33
    ```
    python3 clock_V-1.33.py
    ```
  ![2023-09-29-115719_800x480_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/3639c7f4-7d92-447a-9ac9-791f3278707e)

  2. **Set the Alarm**: Click the 'Set Hour' and 'Set Minute' buttons to set the alarm.

  3. **Alarm Notification**: A pop-up will appear when the alarm rings. Press the stop button to stop the alarm and keep the previoulsy set one, or press the reset button to stop the alarm and clear the previously set one.

  4. **Exit**: Click anywhere on the clock to exit the program.

## Structure:

  **Clock Class**: Inherits from `tk.Tk`.

    - Has methods to draw the clock hands, hour marks, numbers, and check the alarm.

    - Contains button commands to set the alarm hour and minute.

  **cleanup_on_exit**: A function to handle the cleanup process on exit.

## Customization:

  **Colors**: When you want to change the color scheme.

    1. Search for every instance of the mention white, red, blue, and green(on base versions) or purple(on gpio or audio versions).

    2. Paying attention to what each mention of white or purple affects, change to whatever color you'd like

    3. Same applies when changing the background, just search for black instead.

  **GPIO Buzzer Pin**: Only applies to verxion number x.2x!!
    Make sure to change the GPIO pin number to whichever your buzzer is attached to!

    ```
     16--        GPIO.setup(20, GPIO.OUT)
     17--        GPIO.output(20, GPIO.LOW)

    206--        GPIO.output(20, GPIO.HIGH)

    224--            GPIO.output(20, GPIO.LOW)

    235--            GPIO.output(20, GPIO.LOW)
    ```
## Possible changes:

  - Adding the current digital time below the clock for users who prefer a numerical representation.

  - A settings menu to customize the clock's look, e.g., colors, or fonts.

  - Adding a date display (e.g., "Monday, September 29").

  - Integrating the popup window into the program itself as a button that pops up while the alarm is playing.

## Contributing:

  Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License:

  **[MIT](https://choosealicense.com/licenses/mit/)**

---

## *ENJOY!*
