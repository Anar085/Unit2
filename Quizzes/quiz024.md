# Quiz 024




## Code
```.py
from pyfirmata import Arduino
import time

my_ard=Arduino('COM7')

led_green=my_ard.digital[5]
led_red=my_ard.digital[9]
led_blue=my_ard.digital[12]

bit0,bit1, bit2=True,True,True
list_B=[]
list_A=[]
list_C=[]
while True:
    for i in range(8):
        if i%1==0:
            bit0= not bit0
        if i%2==0:
            bit1= not bit1

        if i%4==0:
            bit2= not bit2
        led_red.write(bit1*1)
        led_green.write(bit0*1)
        led_blue.write(bit2*1)
        time.sleep(1)




```

## Proof of work



https://github.com/user-attachments/assets/43c414a6-5041-4576-b60d-100479e33a31




