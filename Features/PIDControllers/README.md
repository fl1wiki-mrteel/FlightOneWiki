# PID Controllers

## SIM Mode

- SIM Mode is a different type of PID Controller that makes the quad feel more aggressive (Bypass PID Controller for the most part?).
- SIM affects all gains (P-I-D)
- SIM Boost should be added as a last tuning step
- SIM and Whisper can be used in conjunction with no issue. 

## Whisper

- Whisper mode is a combined PID controller/mixer combo that makes the quad feel smoother and gives it more authority
- Whisper mode decouples the axises (Roll, Pitch, Yaw). Adjustments to one axis does not affect the other. Keeps axises from fighting each other
- Whisper mode should be added/enabled before PID tuning.
- SIM and Whisper can be used in conjunction with no issue. 
- Whisper mode needs no extra changing of gains (P-I-D) anymore, that was only in legacy code a long time ago it required that (Early versions needed lower D)





# External links
- [Preston explains SIM Mode](https://youtu.be/ltOLWVkZVLA)
- [Betaflight 3.5 VS FlightOne Sim mode Ft. NURK](https://youtu.be/Z2qxnU2SsHM)