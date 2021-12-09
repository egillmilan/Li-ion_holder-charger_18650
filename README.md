# Li-ion_holder-charger_18650
A charger/holder for up to four 18650 lithium-ion battery cells. Charging current is a very conservative 1A, regardless of how many cells are installed. This is due to the input being USB-C and the need for the device to be able to power whatever the batteries power while charging the batteries. The Ideal diode circuit switches the output to 5V from the USB if the charger is connected, otherwise the output comes from the li-ion cells.


**Some technical notes:**
<ul>
    <li>It is VERY important to only charge the same type of cells in parallel (same capacity and manufactuerer) and the cells need to have the same voltage when connected.</li>
    <li>If a charging timer is to be used, an appropriate capacity for C9 can be found in the datasheet and the RSTRT on jumper should be closed.</li>
    <li>C9 can be omitted if no charging timer is necessary, in that case close the CT off jumper.</li>
    <li>A 0.91" OLED and a dip-package ATmega328P can be added to monitor the voltage of the cells while charging, however this is not necessary for the circuit to function properly. If added, the µC on jumper should be closed.</li>
    <li>If no microcontroller is added, R8 can be ignored as it just acts as a pulldown for the ADC when no battery is connected.
    <li>The LED D1 can also be used to monitor the charging status.</li>
    <li>Watch polarity of cells when installed since there is no protection circuit.</li>
</ul>

![Li-Ion_18650_charger](https://user-images.githubusercontent.com/47427510/145484712-5b5a3f1f-26b5-4bb4-bbfa-19440f51af0d.png)
