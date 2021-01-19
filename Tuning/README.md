# Tuning Guide

## Basic tune steps

1. Set Gyro Filters
    1. 5-Inch Freestyle:
        1. Filter stage 1: ~240-300hz
        1. Filter stage 2: ~80-150hz
    1. 5-Inch Race:
        1. Filter stage 1: ~170-240hz
        1. Filter stage 2: ~80-120hz  
1. Set D-term Filters
    1. 5-Inch Freestyle:
        1. D-term Filter stage 1: 200-225hz
        1. D-term Filter stage 2: none
    1. 5-Inch Race:
        1. D-term Filter stage 1: ~225hz
        1. D-term Filter stage 2: ~120hz
1. AI-filter (Cerebro):
    1. If enabled you can raise both GYRO and D-term filter cutoffs
        1. GYRO filter cutoffs increase 50-150hz
        1. D-term filter cutoffs increase ~25-75hz         
1. Enable SIM mode
1. Enable Whisper
1. PIDs
    1. Raise P (2-3 points) and D (10), D value can be 3-20 times the P value, all depending on your filters
        1. Normally you could do ROLL-axis first, then PITCH and last YAW,
            1. Raise P until you get oscillation
            1. Counter P-oscillation by adding D
    1. Add I-term
1. Add SIM Boost
1. Add AA (anti aliasing) if needed


PID-tuning:

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/PID_Compensation_Animated.gif)


# External links
- [WildWilly Tuning Guide](https://youtu.be/9N39QXw_T8I)

