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

### Predictive
A variation of a Dynamic LPF, takes samples and calculates the cutoff frequency


## Filtering explained

### Gyro

We usually need both stage 1 and stage 2 Gyro filters. 

- For a really clean build we can use Frequency for both stage 1 and 2: 
    - Stage 1: Freq @ 300hz
    - Stage 2: Freq @ 150hz
- For a somewhat clean build: 
    - Stage 1: Freq @ 240hz
    - Stage 2: Freq @ 105hz
- For a noisy build: 
    - Stage 1: Freq @ 170hz
    - Stage 2: Dynamic @ 80hz
        - Dynamic filter scale: 80-100

#### Gyro:Stage 1

#### Gyro:Stage 2

### D-Term
Usually only need for one D-Term filter

- For a clean build we can use Biquad for stage 1:
    - Stage 1: Biquad @ 200-225hz
- For a somewhat clean build: 
    - Stage 1: Biquad @ 200hz
    - Stage 2: Biquad @ 200hz
- For a noisy build: 
    - Stage 1: Biquad @ 170hz
    - Stage 2: Biquad @ 80hz    

#### D-Term:Stage 1


#### D-Term:Stage 2


# External links
- [AI/Cerebro - WildWilly](https://youtu.be/tghqr7yJ78I)
- [FlightOne - Filters Part 1](https://www.youtube.com/watch?v=cuwD1KiZQLw)
- [FlightOne - Quickly tune filters and pids](https://www.youtube.com/watch?v=HcopWSx8hYk)
- [UAV Tech Filtering Fundamentals](https://www.youtube.com/watch?v=A09sprstYqI)
- [UAV Tech Filtering Fundamentals Part 3](https://www.youtube.com/watch?v=ULWlDIjha10)