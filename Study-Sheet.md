[\<\-Back](http://euclid.nmu.edu:3000/ovoisine/CS326/wiki)
# Midterm Study Sheet
DISCRIPTION<br>

## Methodologies
#### Methodology:<br>
A set of process and practices of an activity or project<br>

#### 5 Key Values<br>
Simplicity: Maximize value by doing exactly what is expected an no more
Communication: Discussion happens often and includes everyone<br>
Feedback: Take small steps, listen to carefully feedback, make changes<br>
Respect: Everyone contributes and respects those working on the project and their role in it<br>
Courage: tell the truth about estimates, deadlines, costs, and abilities<br>

#### 5 Fundamental Activities<br>
Analysis: Determine requirements<br>
Design: Develop framework for project and current sprint<br>
Code: Create and connect elements of a project<br>
Test: Verify code works as intended<br>
Release: Be able to implement a finalized project in a working state<br>

#### 3 Common Methodologies
Waterfall: Analysis<>Design<>Code<>Test<>Release, too linear, good for small projects with no formal team and no surprises, bad for most other things<br>
Spiral: Analysis>Design>Code>Test>repeat until release, good for nothing (except for maybe a very organized, personal project that won't necessarily see release)<br>
Agile: multiple "sprints" of Analysis>Design>Code>Test>Release until a goal is converged on, requires a good project team manager, good for corporate projects, sprints do not always point directly at the goal, agile can compensate for roadblocks and delays<br>

#### Analysis Patterns
System context: Identify a system boundary by identifying all actors, or every thing that will interact with your system from the outside, such as clients, admins, databases, preexisting or parallel systems, etc.<br>
Use Cases: A list of ways that your software will interact with the actors. Includes 4 things, A name, a list of actors that are impacted by that use case, a description, and other important considerations<br>
Conversations (scenarios): A hypothetical conversation between an actor and a use case, for example<br>
- actor asks system question > system retrieves information > system organizes information > system returns information<br>
- system asks database for information > database returns requested information<br>
LowFi Prototype: A very simple prototype for testing actor interactions with your "software". This should not be stylized in any way, you don't want feedback on how things look or feel, just how it functions. It can even be a pen and paper prototype.<br>
Hotspots: Identify areas that get a lot of use or a lot of complaints.<br>


#### Design Patterns
Canidate Classes: Identify important responsibilities within your system and organize them into classes<br>
Class, Responsibilities, Collaborator cards: A card with the name, role, and responsibilities of a class in your system on it<br>
Object interaction diagram: A diagram that includes a CRC card as the nodes and class/object interactions as lines between them<br>
Class Hierarchies and Interfaces:TBD<br>
Subsystem Diagrams:TBD<br>


#### Architectural Patterns
Layered Architecture: A layered form is a good way to make sure objects are reusable, objects that communicate in the same layer use a "protocol", objects that communicate in different layers use a "interface"<br>
Signal Flow: Describes the process of the flow of information, can be structures as black boxes, with data doing in and a transformed version going out, from one box to another until the data is what is wanted.<br>
Blackboard: ??? "We have a problem that may decomposed spatially into many separate compute domains. We need to scale the computation to a very large size."<br>

#### Design Patterns
Command:???<br>
Observer:???<br>
Model/View/Controller: Models how interaction works between a piece of software and a person. A person exists in one layer, a model, the heart of the system, goes in another and an in between layer contains the view, which shows the person output, and a controller, which allows the person to give input.<br>