
# Tea and Teach: Mermaid

## What is Mermaid
Mermaid lets you create diagrams and visualizations using text and code.

It is a Javascript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.

Basically, you can draw diagrams in Markdown.

## Why should you care?
* It's fun and useful
* It's easy to learn
* It renders in Github so you can take your repo README to the next level
* It's easily modifiable so diagram updates are quick

## Install and run
- [Mermaid Live Editor](https://mermaid.live/) - an online editor 
- VS Code Extensions
    - *Markdown Preview Mermaid Support* -  Adds Mermaid diagram and flowchart support to VS Code's builtin markdown preview
    - *vscode-mermaid-syntax-highlight* - Syntax support for the Mermaid charting language
    - List of [extensions with Mermaid support](https://marketplace.visualstudio.com/search?term=mermaid&target=VSCode&category=All%20categories&sortBy=Relevance)
- Github - just edit a .md file

## Syntax
Use the following:
    `` 
    ```mermaid <some markdown>
    ``` 
    `` to define your drawing

Add in stuff about styles

## Chart types
### graph

```mermaid
graph LR;
A(Get cup) --> B(Add coffee);

```
- Can change the direction of the graph: LR, RL, TB, BT 
- Can label the arrow using | |
- Can extend arrow length
- Can change arrow endings: --o --> --- ==> -.-->
- Can change shapes when adding labels: () [] {} (()) ([])   


A more complex example
```mermaid
graph TB;
A --> B;
F((An input)) --> B;
B{Some decision} -.-> C;
A --> C;
B --- D;
B -->|Yes| E;
E[/Other/] ==>|No| B;
```

### Class diagram
Maybe of more use when describing the workings of code is the class diagram.

In the diagram shown here, the relationships between Animal and Duck/Fish/Zebra are defined, before the properties of the classes. Using a `class` method means that specific parameters can be added and defined per class. 
```mermaid
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


### Pie charts

These are super easy - Mermaid renders the percentage and the legend automatically. 

`showData` is optional and does just that 

```mermaid
pie
    title Number of users of programming languages
    "Python" : 200
    "Rust" : 885
    "C++" : 300
    "Basic" : 95
```

### Gantt charts

Relatively simple to change the section names, dates and task names.

```mermaid
gantt
    title Sparkgeo's Awesome Project
    dateFormat  YYYY-MM-DD
    section Phase 1
    Gather requirements  :GR, 2022-01-01, 15d
    User stories         :after GR  , 20d
    section Phase 2
    Setup AWS                   :2022-01-12, 10d
    Write magic code stuff      :2022-01-18, 20d
    Deliver                     :milestone, 2022-02-10, 0d
```

# What now?
Look at the [docs](https://mermaid-js.github.io/mermaid/#/) as they are very comprehensive

Play around.