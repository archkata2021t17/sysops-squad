{\rtf1\ansi\ansicpg1252\cocoartf2578
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fmodern\fcharset0 Courier;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\paperw11900\paperh16840\margl1440\margr1440\vieww28600\viewh14700\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs26 \cf0 \expnd0\expndtw0\kerning0
# Solution overview\
\
## Principles\
\
1. @TODO\
2. @TODO  \
3. Telemetry is mandatory\
4. @TODO\
\
## Style\
\
Based on provided principles, the system should be n-tier with a layered approach within modules that secure functionality's extensibility. Based on current [business goals](../1.ProblemBackground/BusinessGoalAndScope.md) (number of users, functionality current and desired) and [constraints](../1.ProblemBackground/Constraints.md) the primary implementation style of architecture is **modularized monolith**, with an accent to high modularity to lower cost of further extractions to independent services.\
\
According to declared principles, we propose building systems based on event sourcing and domain-driven design for core components.\
\
@TODO \
\
## Strategic domain design\
\
![Strategic Domain Design](../img/FF_StrategicDomainDesign.jpg)\
\
In the image above, we present our vision of responsibilities for primary system contexts.\
\
**Core**\
\
The main differentiator of the business, unique modules that support business processes. In our case, there are:\
\
@TODO\
\
**Supportive**\
\
\pard\pardeftab720\partightenfactor0
\cf0 @TODO\
\pard\pardeftab720\partightenfactor0
\cf0 \
**Generic**\
\
\pard\pardeftab720\partightenfactor0
\cf0 @TODO\
\pard\pardeftab720\partightenfactor0
\cf0 \
## Conceptual Model\
\
@TODO \
\
\pard\pardeftab720\partightenfactor0
\cf0 @TODO - Meta Model diagram and it\'92s Link\
\
_Knowledge level_ describes rules how actors/entities interact with each other\
\
_Operational level_ describe main actors/entities involved in main scenarios\
\
Metamodel covers all existing business scenarios and should be capable of absorbing future ones. Even more, metamodel should encourage us to think about new scenarios that open in a metamodel.  \
\
Referring to the diagram:\
\
@TODO\
\
## Component composition and communication\
\
@TODO - System Approach diagram and it\'92s Link\
\
*Gravity centers highlighted*\
\
**Aim for Simplicity**\
\
We'd like to provide initial simplicity for the overall system but that do not close the window for further extraction of services and independent development and deployment.\
\
Grouping functional areas to benefit from the ease of development and deployment.\
\
**Aim for Modifiability**\
\
The second important part is to provide points of extensions and ease of modifiability for the proposed solution. It means subparts can be extracted and extended without massive refactoring.\
\
### Composition\
\
@TODO\
\
### Communication and security\
\
@TODO}