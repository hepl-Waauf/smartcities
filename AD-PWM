import machine
import utime

BUZZER = machine.PWM(machine.Pin(20))
POT = machine.ADC(26)


def note(frequence, duree):

    BUZZER.freq(frequence)

    temps = 0

    while temps < duree:

        volume = POT.read_u16()
        volume = volume // 2

        BUZZER.duty_u16(volume)

        utime.sleep(0.01)
        temps = temps + 0.01

    BUZZER.duty_u16(0)
    utime.sleep(0.05)


while True:

    # Ode à la joie

    note(330, 0.30)   # Mi
    note(330, 0.30)   # Mi
    note(349, 0.30)   # Fa
    note(392, 0.30)   # Sol

    note(392, 0.30)   # Sol
    note(349, 0.30)   # Fa
    note(330, 0.30)   # Mi
    note(294, 0.30)   # Ré

    note(262, 0.30)   # Do
    note(262, 0.30)   # Do
    note(294, 0.30)   # Ré
    note(330, 0.30)   # Mi

    note(330, 0.45)   # Mi
    note(294, 0.15)   # Ré
    note(294, 0.60)   # Ré


    note(330, 0.30)   # Mi
    note(330, 0.30)   # Mi
    note(349, 0.30)   # Fa
    note(392, 0.30)   # Sol

    note(392, 0.30)   # Sol
    note(349, 0.30)   # Fa
    note(330, 0.30)   # Mi
    note(294, 0.30)   # Ré

    note(262, 0.30)   # Do
    note(262, 0.30)   # Do
    note(294, 0.30)   # Ré
    note(330, 0.30)   # Mi

    note(294, 0.45)   # Ré
    note(262, 0.15)   # Do
    note(262, 0.60)   # Do

    utime.sleep(0.50)
