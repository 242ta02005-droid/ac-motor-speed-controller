# ac-motor-speed-controller
# AC Motor Speed Controller
# Frequency Control Simulation

print("======================================")
print("       AC MOTOR SPEED CONTROLLER")
print("======================================")

# Motor parameters
rated_frequency = 50       # Hz
rated_speed = 1500         # RPM

# User input
frequency = float(input("Enter supply frequency (Hz): "))

# Check frequency
if frequency <= 0:
    print("\n❌ Invalid frequency!")

elif frequency > rated_frequency:
    print("\n⚠️ Frequency is above the rated value!")
    print("Motor speed control limit exceeded.")

else:
    # Calculate approximate speed
    speed = rated_speed * (frequency / rated_frequency)

    print("\n--- Motor Status ---")
    print("Supply Frequency :", frequency, "Hz")
    print("Motor Speed      :", round(speed, 2), "RPM")

    if frequency < rated_frequency:
        print("🟢 Motor speed reduced")

    elif frequency == rated_frequency:
        print("🟢 Motor running at rated speed")

    print("⚙️ AC Motor Controller Operating")
