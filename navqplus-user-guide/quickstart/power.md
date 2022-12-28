# Power

![](<../../.gitbook/assets/image (1) (1).png>)

There are two ways to power NavQPlus. You can power it through the PWR\_IN port or through the USB-C port in the middle.

\
**It is preferred to power the board from PWR**_**IN connection for highest reliability.**_\
_****_This is because it is possible that the USB-C logic may be configured in software in a manner that limits current. This leads to unexpected behavior at power up. If you suspect something is "wierd" on power up or you see rebooting of the board, please try powering from PWR\_IN first.&#x20;

The PWR IN port accepts and input in the 6V-20V range. (Technically should work from 5V to 29V, but has not been fully characterized)

The PWR IN port pinout schematic is as follows: (center pin is unused)

![](<../../.gitbook/assets/image (4) (1).png>)

With Pin 1 being the top pin in the image above. PWR\_UNREG is just 5-20V power.\
\
\


{% hint style="info" %}
&#x20;If you encounter unexpected resets, it could be that your power supply is not able to provide enough current for the board or the board+peripherals resulting in a brownout condition when some block/interface/peripheral turns on and draws additional current.\
Supplying power with a LiPo battery may help debug if you have a bench or wall adapter power supply limitation.  &#x20;
{% endhint %}