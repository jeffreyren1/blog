---
layout: post
title: Plantuml Example
author: Jeffrey
categories: example
tags: [plantuml,example]
top: 2   <!-- DO NOT USE top:2, USE top: 2, LEAVE A WHITESPACE -->
banner:
  video:
  loop: 
  volume: 
  start_at: 
  image: /assets/images/bingpic/BathCircus.jpg
  opacity: 0.9
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
---


---
layout: post
title: Welcome Back
author: Jeffrey
categories: misc

---


## PlantUML Block-1

@startuml
Bob -> Alice : hello
@enduml

## PlantUML Block-2

``` plantuml!
Bob -> Alice : hello world
```

## PlantUML Block-3

@startuml
(*) --> "Initialization"

if "Some Test" then
  -->[true] "Some Activity"
  --> "Another activity"
  -right-> (*)
else
  ->[false] "Something else"
  -->[Ending process] (*)
endif
@enduml

## PlantUML Block-4

@startuml
skinparam handwritten true

skinparam usecase {
  BackgroundColor DarkSeaGreen
  BorderColor DarkSlateGray

  BackgroundColor<< Main >> YellowGreen
  BorderColor<< Main >> YellowGreen

  ArrowColor Olive
  ActorBorderColor black
  ActorFontName Courier

  ActorBackgroundColor<< Human >> Gold
}

User << Human >>
:Main Database: as MySql << Application >>
(Start) << One Shot >>
(Use the application) as (Use) << Main >>

User -> (Start)
User --> (Use)

MySql --> (Use)

@enduml
