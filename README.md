# meian-hacking
Shenzhen Meian Technology safety alarm systems hacking

For many people asking me about [meian-client](https://github.com/wildstray/meian-client) and [meian-dissector](https://github.com/wildstray/meian-dissector) and how I obtained the encryption keys.

Here in Italy we call it a Pulcinella's secret :smile: I decompiled the apk of the Android App. Looking into java code I cannot find anything userful. So I targeted the dynamic libraries. The Jackpot is into **libComCore.so**.

![Ark](https://github.com/wildstray/meian-hacking/blob/main/images/ark.png)

Then I used [Binary Nija](https://binary.ninja/) to analyze it. The Free version is enough :wink:

I found the functions Encode and Decode...

![Encode](https://github.com/wildstray/meian-hacking/blob/main/images/encode.jpg)

![Decode](https://github.com/wildstray/meian-hacking/blob/main/images/decode.jpg)

![Decode low](https://github.com/wildstray/meian-hacking/blob/main/images/decode_low.jpg)

![Decode med](https://github.com/wildstray/meian-hacking/blob/main/images/decode_med.jpg)

...and here is the keys :wink:

![szTable](https://github.com/wildstray/meian-hacking/blob/main/images/szTable.jpg)
