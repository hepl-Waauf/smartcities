import machine
import utime

LED = machine.Pin(16, machine.Pin.OUT)
BUTTON = machine.Pin(18, machine.Pin.IN)

val = 0
ancien_etat = 0

while True:

    etat_bouton = BUTTON.value()

    if etat_bouton == 1:
        if ancien_etat == 0:
            val = val + 1
            print(val)

    ancien_etat = etat_bouton

    if val == 1:
        LED.value(1)
        utime.sleep(1)
        LED.value(0)
        utime.sleep(1)

    elif val == 2:
        LED.value(1)
        utime.sleep(0.1)
        LED.value(0)
        utime.sleep(0.1)

    elif val >= 3:
        LED.value(0)
