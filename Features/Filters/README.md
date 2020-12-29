# Filters

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/FLX_Filter_001.JPG)

## Gyro filters

- AI (Cerebro)
- Frequency ("Freq")
- Biquad
- Dynamic
- AA / Anti Aliasing 

## D-term filters
- Frequency ("Freq")
- Biquad
- Dynamic
- AA / Anti Aliasing 


### AI Cerebro
A type of AI based dynamic filter
- lets you raise stage 1 and stage 2 filter cutoffs by 25% 
    - for eg from 240hz to 300Hz, or 105hz to 130hz
    - Start by raising the cutoff by 25hz at a time, check for hot motors.

![Image](https://github.com/fl1wiki-mrteel/FlightOneWiki/blob/main/IMG/H7_EnableCerebro.JPG)

### Frequency
Static frequency filter (PT1?), faster then Biquad

### Biquad
Filters more then frequency filter (?)

### Dynamic
Set your filter Hz and set how much it should filter with "Dynamic filter scale"  default is 80.

### AA / Anti Aliasing
Used for noisy builds, can help remove some of the last noise

Available values:
- Dynamic AA: Enabled/Disabled
- AA Strength: off, low, mid, high



## Filtering explained

### Gyro

#### Stage 1, Stage 2

### D-term

#### Stage 1, Stage 2


# External links
- [AI/Cerebro - WildWilly](https://youtu.be/tghqr7yJ78I)
- [FlightOne - Filters Part 1](https://www.youtube.com/watch?v=cuwD1KiZQLw)
- [FlightOne - Quickly tune filters and pids](https://www.youtube.com/watch?v=HcopWSx8hYk)
- [UAV Tech Filtering Fundamentals](https://www.youtube.com/watch?v=A09sprstYqI)
- [UAV Tech Filtering Fundamentals Part 3](https://www.youtube.com/watch?v=ULWlDIjha10)