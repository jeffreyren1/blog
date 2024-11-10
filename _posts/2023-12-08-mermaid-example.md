---
layout: post
title: Mermaid example
subtitle: my first blog
author: Jeffrey
categories: example
tags: [mermaid, example]
top: 
banner:
  video: https://vjs.zencdn.net/v/oceans.mp4
  loop: true
  volume: 0.5
  start_at: 8.5
  image: /assets/images/bingpic/FloresIsland_1920x1080.jpg
  opacity: 0.618
  background: "#000000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"


---

## 1. Pie chart

```mermaid!
pie title Pets adopted by volunteers
  "Dogs" : 386
  "Cats" : 85
  "Rats" : 35
```

## 2. sequence diagram

@startmermaid
sequenceDiagram
  Alice ->> Bob: Hello Bob, how are you?
  Bob-->>John: How about you John?
  Bob--x Alice: I am good thanks!
  Bob-x John: I am good thanks!
  Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.
  
  Bob-->Alice: Checking with John...
  Alice->John: Yes... John, how are you?
@endmermaid
 
 
```mermaid!
graph TD
A[Christmas] -->|Get money| B(Go shopping)
  B --> C{Let me think}
  C -->|One| D[Laptop]
  C -->|Two| E[iPhone]
  C -->|Three| F[fa:fa-car Car]
```

## 3. Class diagram
```mermaid!
classDiagram
Animal <|-- Duck
Animal <|-- Fish
Animal <|-- Zebra
Animal : +int age
Animal : +String gender
Animal: +isMammal()
Animal: +mate()
class Duck{
  +String beakColor
    +swim()
    +quack()
}
class Fish{
  -int sizeInFeet
    -canEat()
}
class Zebra{
  +bool is_wild
    +run()
}
```

## 4. State diagram
```mermaid!
stateDiagram
[*] --> Still
Still --> [*]

Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]
```
