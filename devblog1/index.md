# Game Dev Blog #1: Dialogue Screen

Making a game as hard AF. 15 hours in, and I have managed to scrape (and I mean scrape) together a somewhat working dialogue screen with one character speaking. 

<!--more-->

Maybe I am a terrible Googler or maybe I am just naive, but with the popularity of Monogame, I was hoping there would be more official documentation on default implementation for classic game features (ex. dialogue trees). Moving forward, I will definitely try searching through Github for examples.

*Assets are all from **Ace Attorney**, for now.*

{{< figure src="/images/post/devblog1/phoenix-demo.gif" >}}

### Features
1. Automatically reads dialogue from text file
2. Animates speaker depending on line spoken
3. Distinguishes between animations that loop and animations that do not
4. Can click mouse to skip to end for longer text

### Next steps
1. Better organize current code
2. Change dialogue reader to XML file
3. Implement dialogue screen to swap between 1 or 2 speakers
4. Wrap dialogue text

---
### Implementation Details
---
For the game, I've decided to use Monogame, without the Monogame.Extended library, since I did not need any of the 3d or physics features (and I could not figure out where the SpriteSheetAnimationFactory class went... haha).

Below is the PlantUML class diagram. Not all methods and attributes within a class have been included for brevity's sake.
![UML class diagram](/images/post/devblog1/uml_cd.png "PlantUML class diagram")

**Best resources I've been using**:
1. [Microsoft XNA Documentation](https://docs.microsoft.com/en-us/previous-versions/windows/xna/bb200104(v=xnagamestudio.41))
2. [StackExchange](https://gamedev.stackexchange.com/)
3. [Leshy's SpriteSheet Tool](https://www.leshylabs.com/apps/sstool/)
