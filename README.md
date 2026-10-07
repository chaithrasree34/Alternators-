# Alternator Calculator Using Python

import math

print("ALTERNATOR CALCULATOR")
print("---------------------")

print("1. Calculate Generated EMF")
print("2. Calculate Frequency")
print("3. Calculate Synchronous Speed")
print("4. Calculate Output Power")
print("5. Calculate Efficiency")

choice = int(input("\nEnter your choice (1-5): "))

if choice == 1:
    Kc = float(input("Enter pitch factor (Kc): "))
    Kd = float(input("Enter distribution factor (Kd): "))
    Phi = float(input("Enter flux per pole (Wb): "))
    T = float(input("Enter turns per phase: "))
    f = float(input("Enter frequency (Hz): "))

    E = 4.44 * Kc * Kd * Phi * T * f

    print("\nGenerated EMF =", round(E, 2), "V")

elif choice == 2:
    P = int(input("Enter number of poles: "))
    N = float(input("Enter speed (RPM): "))

    f = (P * N) / 120

    print("\nFrequency =", round(f, 2), "Hz")

elif choice == 3:
    f = float(input("Enter frequency (Hz): "))
    P = int(input("Enter number of poles: "))

    Ns = (120 * f) / P

    print("\nSynchronous Speed =", round(Ns, 2), "RPM")

elif choice == 4:
    V = float(input("Enter line voltage (V): "))
    I = float(input("Enter line current (A): "))
    pf = float(input("Enter power factor: "))

    power = math.sqrt(3) * V * I * pf

    print("\nOutput Power =", round(power, 2), "W")
    print("Output Power =", round(power / 1000, 2), "kW")

elif choice == 5:
    output# Alternators-