# Game Dev Blog #2: Dialogue Struggle Bus

After spending approximately 4 hours failing to deserialize my XML dialogue, I decided I hated the lack of Monogame resources and attempted a brief flirtation with Unity, believing it would be more streamlined. It was not. 

<!--more-->

I spent over 5 hours trying to figure out how to work the camera (yes, I very stupid), and since our current game plans do not even include a camera, I did not think the bells and whistles of Unity was worth it.

Back in Monogame, I completely gave up on XML, and I moved forward with JSON.

*Assets are all from **Ace Attorney**, for now.*

{{< figure src="/images/post/devblog2/phoenix-demo.gif" >}}

### Features
1. JSON file reader for dialogue events
2. Events connected to main character's stats, relationships, and previously seen events
3. Events support 0 - 2 character animations on screen
4. Events support audio (sound effects & background music)

### Next steps
1. Add support for choices and outcomes during events
2. Wrap dialogue text
3. Start work on menu/stat-raising game mechanics

---
### Implementation Details
---
The JSON file maps to an AllEventDialogue object will, in theory, house all of the event dialogue in the game. Each EventDialogue object has a list of relationships, stats, and flags which determine when the event will be played. The event text follows a basic script which determines the event's background images, animations, dialogue, and main character status changes.

Currently, I plan on using a GameplayManager object to control when events play (vs when other gamplay is occurring). TBD as to whether or not that will work.

**Updated and Condensed UML Diagram**

![Refactored to use interface](/images/post/devblog2/uml_cd.png "PlantUML class diagram")

**Example JSON Text**

```
*witnessempty\n
%ost/gumshoe\n
It seems like Phoenix is sick.\n
Oh here he comes!\n
@redgeworth\n
Acchoo! @lphoenix #sneezing\n
```

**Best new resources I've been using**:
1. [JSON Formatter](https://jsonformatter.org/json-editor)
2. [Remove/Replace Line Breaks](https://www.gillmeister-software.com/online-tools/text/remove-line-breaks.aspx)

**Resources from prior developments**:
1. [Microsoft XNA Documentation](https://docs.microsoft.com/en-us/previous-versions/windows/xna/bb200104(v=xnagamestudio.41))
2. [StackExchange](https://gamedev.stackexchange.com/)
3. [Leshy's SpriteSheet Tool](https://www.leshylabs.com/apps/sstool/)
