# Presentation Demo-Day


## What is Android Automotive

- New Operation System from Google
- Android Based for Cars
- not to be confused with Android Auto
- first Car is the Polestar 2 from Volvo coming later this year
- The Car View only supports Media Apps with Messenger Apps are on its way

## Goal of the project

- gain expierience with Android Automotive
- create three Apps and a Launcher
- summarize limitations and opportuinites of the platform
- work together with IAV

## Difficulties

- Research focus
- API still under Development
- limited public documentation
- working as a Team is difficult when working on three independent projects

## Launcher Story

- IAV mockup with three parallel apps 
- Research different implementation frameworks

### Our Launcher

- Fork standard Automotive OS Launcher
- immediately encountered permissions problems 
- deployment not possible as system App 
- we build our own rooted system image with the Android Open Source Project
- decompile Volvo launcher who actually neither overcame existing problems
- decision to stop there and handover to IAV
- no steady progress, mainly research and hacking
- difficult to quantify sprint goals 
- difficult sprint planing

### IAV Launcher

- IAV build upon our results on created that ->

## Trip Computer App

- Goal: acquire and display values from hardwareinterface (Car Data)
- Again permission problems 
- Research how to circumvent these
- App is a standard Android App because AAOS only supports media apps -> 

## Podcast App
- explain difference automotive view / standard app
- build upon open source podcast player Antennapod
- extend to match googles requirements for AAOS
- (Pull Reqeust to upstream the changes)

### Messaging App
- Create standalone messaging app to experience Scrum Process as a Team 
- not really Android Automotive OS specific
- created frontend and backend 

