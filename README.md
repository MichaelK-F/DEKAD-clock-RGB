# Adding RGB to the Ikea DEKAD clock
Currently unfinished guide on how to add RGB lights to the Ikea DEKAD clock.
[Ikea DEKAD clock online store link](https://www.ikea.com/au/en/p/dekad-alarm-clock-black-10540480/)

## TODO:
 - [ ] Add dissasebly guide.
 - [x] Instructions on adding RGB led strip.
 - [ ] Instructions for mounting ESP8266 and making entire clock USB powered.
 - [ ] Instructions for software/firmware.
 - [ ] Table of contents.


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



Instructions on mounting ESP8266 coming soon!
