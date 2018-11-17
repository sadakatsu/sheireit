# Sheireit
## Concept
Sheireit (ʃeɪ'ʁeɪt) is a prototype for an all-in-one tabletop game design tool.  My goal is to make a program that can help a game designer fully prepare a raw idea for game development, hopefully for a smooth and quick process before publishing.  The features I envision the final product having are:

1. A complete GUI for designing virtually every type of tabletop game, using wizards, drag-and-drop diagrams, file attachments for adding visualization for components, and a minimum of text entry.
1. A game engine for running games built in this system, capable of running games single player against AIs, hotseat, and multiplayer with servers.
1. A simple raw text format for describing nearly all the game's data so that projects can be easily saved (will likely use [JSON Schema](https://json-schema.org/)).
1. Version control built on top of [Git](https://git-scm.com/) so designers can easily try out different ideas simultaneously or collaborate with others on a project; will provide UI views for handling pull requests and merge conflicts
1. Automated playtesting by AIs with configurable training periods and game counts, resulting in statistical views to highlight problems with the design (research goal)
1. Servers to allow game designers to temporarily release one or more versions of their games so alpha testers can find, play, and provide feedback on their experiences
1. Local database for storing playtest data, including complete logs of the games, reasoning generated by the AIs (if any), and tester feedback (if any); can persist locally-generated data to origin server so the lead can review results
1. Game design analysis using ideas from code analysis metrics to highlight areas where the game should be simplified (research goal)
1. Game design analysis to detect and name patterns used to help attach tags a designer can use to describe his game (research goal)
1. Button-press manual generation to guarantee exact, precise, and concise rules that eliminate duplication and conflicting descriptions of mechanics.

I think that such a tool could get a game design to the point that a pitch to a publisher should be much more certain to succeed.  I think that game designers would be delighted to send publishers their prototypes with clear manuals for thoroughly tested designs, play test summary data for thousands of games, and endorsements from dozens of play testers.  Even better, I suspect that this program would catch on with publishers as well, so designers could share their complete design with the publisher by giving the publisher access to their projects' repositories.

My plans for this application are very ambitious.  Sheireit is my attempt to start small, providing a tool that I hope will still be useful without the other features.  For this spike to succeed, Sheireit must:

- allow game designers to build a tabletop game completely through the UI as in goal #1 above
- provide a game engine for running the hotseat games designed in it as in goal #2 above (AIs and server multiplayer can wait)
- save game designs using a simple data format as in goal #3 above

I figure these three features alone would improve on what I have currently found available.  [Vassal](http://www.vassalengine.org/) allows people to create games and play them with people, but the community seems most interested with creating implementations of already published games.  [boardgame.io](https://boardgame.io/) allows programmers to build tabletop games with JavaScript, including OOTB multiplayer servers and AIs, but it does not provide friendly tools for designers who do not know how to program to build their games.  I am impressed by both these offerings, but I also think that Sheireit would be a first step to offering something oriented toward game designers.

## Build Instructions
This is a fairly high-level overview of these steps.  I might provide more detailed instructions in the future; for now, I am trying to make forward progress  :/

1. If you do not have it already, install JDK 8 or greater on your system.
2. If you have not already done so, set the `JAVA_HOME` environment variable to the root directory of your JDK installation.  For example, on my system, that is `D:\Program Files\Java\jdk1.8.0_152`.
3. If you do not already have it, install git.
4. If you have not already done so, and you are a Windows user, make sure that the directory that holds `git.exe` is on your PATH.  For example, on my system, it is `C:\Program Files\Git\cmd`.
5. Choose a place on your system to hold Sheireit.
6. Navigate to that directory in a terminal.
7. Run `git clone https://github.com/sadakatsu/sheireit.git`.
8. Enter that directory.
9. Run `gradlew bootRun`.  The first time you run this, it can take a long time.
10. Once you see a message like `2018-11-17 15:32:49.950  INFO 12376 --- [           main] c.s.sheireit.SheireitApplication         : Started SheireitApplication in 1.388 seconds (JVM running for 1.735)`, open your browser and navigate to [localhost:8080](http://localhost:8080).
11. Start using Sheireit!


**More material will come as I start committing code.**
