# Adding RGB to the Ikea DEKAD clock
Guide on how to add RGB lights to the Ikea DEKAD clock.

![20240825_200420](https://github.com/user-attachments/assets/b51358c9-3fc3-462f-91e2-f280fd148843)

## Where to buy:
 - [Ikea DEKAD clock](https://www.ikea.com/us/en/p/dekad-alarm-clock-black-30540479/)
 - [Wemos D1 mini](https://www.aliexpress.com/item/32529101036.html) The one here is a newer version with USB-C but it should work just fine
 - [M4-5H relay](https://www.aliexpress.com/item/32246573811.html) I did NOT buy from this seller so you might be better off finding a different place to buy it
 - [DC-DC buck convertor](https://www.aliexpress.com/item/1005006494548995.html) This is not the same one that I used but it has the same specs
 - [WS2811 LED strip](https://www.aliexpress.com/item/1005006961233629.html) 

## Disassembly instructions

Remove battery cover and batteries before starting.
Remove three screws on the back of the clock and remove the back cover. Note: these screws are longer than all of the other screw
![20240731_191900](https://github.com/user-attachments/assets/8177e4dd-a0a0-45df-ad6a-5d4d17cac262)

Remove the four screws holding in the switch and the alarm motor, then lift out the battery holder.
![20240731_192039](https://github.com/user-attachments/assets/9da01b05-6fb4-4d7c-baa2-d3131d69be92)

Remove the plastic pin holding the the alarm bell arm, followed by the arm itself.
![20240731_192303](https://github.com/user-attachments/assets/e617eaaa-b122-4386-88ce-fb0629741743)
![20240731_192449](https://github.com/user-attachments/assets/be0c22bd-6779-458d-8a5a-7205aae093d6)

Remove the nut holding in the handle and the bells, then remove the handle and the bells.
![20240731_192600](https://github.com/user-attachments/assets/0338527d-4792-4b25-82e9-5379a5de98f4)

Remove the feet.
![20240731_193109](https://github.com/user-attachments/assets/b453b442-999a-4cbd-b3c7-7a31722e9d16)

You should have a pile of parts that looks something like this.
![20240731_193232](https://github.com/user-attachments/assets/00226206-fd97-4cbc-a0d4-c3949c31a7cf)

Now you can lift everything out of the clock like this.
![20240731_193423](https://github.com/user-attachments/assets/3e41faa5-571e-4347-ab76-5a68e62d00a2)

You are now ready to add RGB to your clock!


## How to add the RGB

Once the Clock is dissasembled (instructions coming soon), you will need to remove the clear plastic ring that keeps a gap between the glass and the clock hands.
![20240728_202406](https://github.com/user-attachments/assets/65a5620a-5aad-4e04-8527-04ab4d36eca6)

Cut a length of leds that will fit the ring. I managed to get 17 to fit, but with a different led strip you might be able to get more or less.
![20240728_201937](https://github.com/user-attachments/assets/b8e5f21a-a036-4d9e-ae07-3638b2eb0a7d)

For most led strips, they will be too wide. If your led strip is a few mm narrower than 10mm you might be able to skip this step.
To accomodate for the width of the led strip, carefully snap off the plastic sticking out the side using pliers as seen in the photo.
![20240728_202531](https://github.com/user-attachments/assets/e22438ee-08f0-4241-be27-a290d14b938f)

After removing the plastic that gets in the way, the plastic ring should look somthing like this (You can see that I accedently snapped part of it, but you can't see it when fully assembled):
![20240728_203704](https://github.com/user-attachments/assets/78f20e97-17a4-4488-be19-baa331cca1e1)

Now would be a good time to do a test fit. As you can see it fits:
![20240728_203516](https://github.com/user-attachments/assets/ff8b1bcf-fd84-45ac-a0d5-559f1cc46640)

Now, time for soldering. If your led strip has a plastic protective layer, carefully peel it up.
![20240728_205034](https://github.com/user-attachments/assets/6f04ba62-c76b-4bf6-bd2f-037a413d801a)

Tin the wires and the led strip pads.
![20240728_205806](https://github.com/user-attachments/assets/9501b8d2-bd77-4791-b4f0-df76d4f49c31)

Solder the wires to the led strip (yes I know that isn't the best soldering job).
![20240728_210237](https://github.com/user-attachments/assets/133f232e-bfd3-44c6-b89c-3db31ebc6ac7)

Use a bit of hot glue to insulate the connections (you might also need to trim some of the protective layer if your led strip has it because it might be too thick to fit).
![20240728_211045](https://github.com/user-attachments/assets/517c8833-caed-4f15-bcae-7e54b4d92e99)

Time for a test fit (I aligned the wires with the top of the clock so they are not as obvious).
![20240728_211701](https://github.com/user-attachments/assets/6d0d1ae8-2195-4159-86c2-7fbc278faf6b)

It works!

![it works](https://github.com/user-attachments/assets/0f2057e2-5796-4a35-a950-c7dc0d969405)


To make a place for the wires to go, I used a soldering iron to melt a small channel. WARNING: Plastic fumes are toxic. Make sure to do this in a well ventilated area.
![20240728_213152-trim](https://github.com/user-attachments/assets/a63fcf06-e80f-46bc-b742-625e04117ac4)

The wires routed through the channel:
![20240729_190545](https://github.com/user-attachments/assets/75b9996f-0601-4de7-8903-c847f8e3b1db)

What it looks like once the clock has been mostly reassembled:
![almost final](https://github.com/user-attachments/assets/0cef9825-ff27-426e-9224-be873367c38c)


## Adding ESP8266, relay and making it USB powered.

Desolder the components as shown:
![20240805_211011](https://github.com/user-attachments/assets/3d334e92-94aa-4fc2-90c2-f85fa469ac2c)

**WARNING! Before soldering in the buck converter, you must connect it's output to a multimeter and it's input to a 5V source then turn the potentiometer until the multimeter reads 1.5V. If you do not do this, there is a risk of damaging the clock.**

Connect the output of the buck converter to where the battery was previously connected as shown:
![20240805_213210](https://github.com/user-attachments/assets/5c2154c3-8f37-489a-9ae1-cbc45443a527)

### The relay:
![20240805_213526](https://github.com/user-attachments/assets/73ee5a11-6ad6-4f2d-964c-4c5008dceb75)
![20240805_213539](https://github.com/user-attachments/assets/50f3bf11-6e3a-4f58-9042-c61071d2d173)
[Datasheet](https://github.com/user-attachments/files/16676423/M4-5H.pdf)

Solder the relay inline, connected to C1 and NC1 (direction does not matter).
![20240805_215234](https://github.com/user-attachments/assets/92ef7e2a-d7e6-45ec-af91-c934a49a80f3)

Solder a wire (yellow in photo) from NC1 to NO2.
![20240805_220110](https://github.com/user-attachments/assets/dcfdeb64-0ebf-43ff-9e1d-f906c11b31da)

Solder a wire from C2 to the negitive terminal of the clock, followed by connecting the positive terminal of the motor to the positive terminal of the clock. Finally, connect the negitive terminal of the motor to NC1 or NO2.  
![20240806_175916](https://github.com/user-attachments/assets/b28ed37e-8b57-4388-9a39-fab4e1afa8af)

Solder one wire to each of the coil contacts for the relay.
![20240810_215440](https://github.com/user-attachments/assets/5041102f-0e8d-4c65-a234-8ad6230786d3)

Temporarly screw the motor back underneath it's bracket.
![20240810_215546](https://github.com/user-attachments/assets/b4b2bf8f-303a-4ca3-b458-f8cf6bf6434e)

Solder all of the 5V positive wires together (from the led strip and the buck converter), then solder one more wire as shown in the photo. Repeat the same steps for the negitive wires (the led strip, buck convertor and the relay).
![20240812_130843](https://github.com/user-attachments/assets/bd5582d7-871f-4783-baba-a4e126137412)

Cover up the connections to prevent any shorts from occuring.
![20240812_132236](https://github.com/user-attachments/assets/c9242e27-5c5e-4984-9b51-253dac08abcc)

Connect the combined 5V wire to the 5V pin of the Wemos D1 mini (ESP8266), the negitive wire to the GND pin, the remaining relay wire to D1 and the LED strip data pin to D2.
![20240812_180853](https://github.com/user-attachments/assets/ff343316-7e34-4ca3-8b74-083aeac78114)

Screw the switch back into place.
![20240812_154635](https://github.com/user-attachments/assets/568552fb-0cbd-478e-a983-f5145637c9f9)

Use hot glue to hold the relay and the buck coverter in place.
![20240812_165338](https://github.com/user-attachments/assets/3d153268-da11-4771-af27-ed4926bb3fa2)

Put the clock assembly back together and make sure it still fits.
![20240812_181850](https://github.com/user-attachments/assets/34a9c087-f771-4afb-92b9-0643b243d9f1)

Unscrew the motor to route the wires for the LED strip, then put in the bell arm and its retaining pin, followed by screwing the motor back in.
![20240812_182517](https://github.com/user-attachments/assets/9fb7b5a6-8c6e-475f-a006-bf83cf1bcb2f)
![20240812_182856](https://github.com/user-attachments/assets/7142adfc-a756-4000-bcb9-9c43b806a9e9)

Connect a usb cable (make sure it is a data cable, not just a power cable) to the ESP8266 before hot gluing it into place.
![20240812_183432](https://github.com/user-attachments/assets/8baf879b-de92-4517-93d6-c8d4689ffe07)

Screw the back back on and route the USB cable through the battery hole.
![20240812_183707](https://github.com/user-attachments/assets/d60be87a-73f2-4521-adb6-f30f31077508)

Make a small hole for the usb cable in the battery cover.
![20240812_184904](https://github.com/user-attachments/assets/8de6fa1d-dcc5-4c80-b8e1-a5f9b17226b7)
![20240812_185406](https://github.com/user-attachments/assets/7afced76-c874-436f-bdb1-b94da937ac76)
![20240812_185516](https://github.com/user-attachments/assets/e35efa29-c05c-4827-b922-99832a07def0)

## Firmware/Software options
WLED vs. ESPhome(HomeAssistant)
If you want to control the relay and/or already have [Homeassistant](https://www.home-assistant.io/) set up, using the ESPhome addin is the best route to take.
If you don't have a homeassistant server or want to have a clock that reacts to music using [LedFx](https://www.ledfx.app/), then [WLED](https://kno.wled.ge/) is the best route to take (it still has a homeassistant integration if you want it).

### WLED firmware install
Follow the [WLED installation guide](https://kno.wled.ge/basics/getting-started/).
One installed, change the led strip pin to D2 (the default is D4), and change the number of LEDs to 17 (or however many you managed to fit).
If you want to have a sound reactive clock, then download [LedFx](https://www.ledfx.app/download-ledfx/)

### Using Homeassistant and ESPhome addin
These instructions assume you have already set up Homeassistant and ESPhome, and have a basic knowledge of how to use ESPhome.
Create a new device in ESPhome and flash it over USB from your computer.
Edit the yaml file and add the following config to the end of it:
```
light:
  - platform: neopixelbus
    type: GRB
    variant: WS2811
    pin: D2 #Change this if you used a different pin
    num_leds: 17 #Change this if you have a different number of LEDs
    name: "NeoPixel Light" #You can change the name of the light in Homeassistant here
    default_transition_length: 
      seconds: 0.2 #If you set it to a longer time period if can sometimes flicker in undesierable ways
    effects: #To add more effects, go to: https://esphome.io/components/light/index.html#light-effects
      - addressable_rainbow:
          width: 17 #If you set this to the same number of leds that you have, the effect will look the best

switch:
  - platform: gpio
    pin: D1 #If you used a different pin for the relay, change it here
    name: "Alarm" #You can change the name of the alarm in Homeassistant here
```
You should now be able to install the config OTA and the LED strip and alarm should show up in Homeassistant.

## Moded vs. stock clock
![20240825_200428](https://github.com/user-attachments/assets/c2ee55ae-f198-4127-ba94-069fca353cd4)
![20240825_200420](https://github.com/user-attachments/assets/b51358c9-3fc3-462f-91e2-f280fd148843)









 
