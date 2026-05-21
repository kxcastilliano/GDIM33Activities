<img width="1206" height="855" alt="Updated Breakdown" src="https://github.com/user-attachments/assets/06d196ad-3085-41a5-bcb1-173e2f23e565" />
# GDIM 33 In-Class Activities
## W1
### Activity 1

[Link to Mood Board](https://pin.it/3FpnkK9Ln)

1. Looking at my moodboard some things that sparked similarity is my love for narrative heavy games. I love games with memorable/loveable character designs/lore with hints of social commentary/psychological undertones. 
I am stuck looking for visuals or a good plotline for this game since I love a lot of various different aesthethics. a lot of my creative ideas are I take great iunspiration from songs I like so just having some time to myself 
I'll have time to daydream and visualize potential ideas for this project. 

2. Looking at my table mates ideas we seem to have a lot of aestheitc differences visually, some are horror fans and some like more action based games rather than visual novels. 

3.  Similarly, LAs appears to enjoy more action based and serious toned games- much different than the whimsy approach I want to take. 


### Activity 2

<img width="960" height="720" alt="Breakdown Ver 1  (1)" src="https://github.com/user-attachments/assets/b293ab76-a00b-4039-a6ff-d1d690913c8b" />





## W2


## W3

### Activtiy 1

<img width="1206" height="855" alt="Updated Breakdown" src="https://github.com/user-attachments/assets/0e3c3950-d5f7-4861-b37f-c075169f81d7" />

### Activity 2

#### Question 1 

It is advantageous to save the event name for the explore-to-dialogue state transitions as a Scene variable as it makes the event easy to reference within other graphs for example by making it a scene variable we could input it into the walrus' graph.

#### Question 2

I had used Debug.log nodes for two instances, checking to see if the game was registering when the mouse was clicked and to see if the transitions were working. By putting Debug.log I was able to easily identify what the root of my problem was when I saw that certain things weren't processing in the game:
by seeing that the console was registering each mouse click I was able to understand that th issue wasn't with the on click event but with the calling of the transition. 

#### Question 3

Since my game is 2d and lacks any movement of any sort, I do not believe that set cursor lock state will be relevant in the architecture of my game. 

### Question 4

The concept of a game state could be relevent to my game and it's something I'm considering adding in turns of making a state machine active in the game: In my game I plan to have two states that activate at the end but are able to change as the player 
gains or loses points to their friendship meter, by tracking their points the value will determine if they are at the state that will lead to the good ending and the state that will lead to the bad ending. 

## W4

### Activiy 1

#### playtest goals
So far in my current build I have a simple dialogue sequence/gameplay, there are no choices implemented yet so for now in terms of a playtesting goal, I want to check with group if 
this system seems smooth and if the game (though character art isn't implemented) feels engaging. 

#### playtest team members
Alejandra, Laura, Bilal.

#### playtest notes
- Dialogue runs smoothly
- likes how the UI flips to accomodate for the character who is speaking.

### Actiity 2

#### Question 1

In the event a writer wants to add more dialogue to the set up, they will be able to do this without the event of any coding due to the dialogue nodes being managed as scriptable objects in the game's inspector.

#### Question 2

I believe there is no limit to how much dialogue can be made without any coding involved due to a. the use of ScriptableObjects being used and b. the fact that the script graph is constantly checking nodes and registering it's reply option plus what the reply options each lead to within a for loop node. 

#### Question 3

Regenerating Nodes helps new nodes be able to properly process. When we create new variables and methods it's important to regenerate nodes so unity can look through it's list and realize that it didn't make any nodes for these new things added and as a result of regenerating unity will have these nodes made for us.


## W5

### Activity 1
Using Tineline to create a sequenced cutscene

#### Creating a starting cutscene

1. Create a new scene to put cutscene in 
2. Download and install timeline (if package isn't downloaded)
3. Window -> sequncing -> Tinmeline to create a tinmeline in scene
4. Create timeline and save somewehre within Asset folder 
5. Create gameobjects for Image UI you want in cutscene
6. Right click on timeline and ass an animation track
7. drag image in animator spot of timeline
8. Click Record, drag animations by the amount of frames you want animation to run and lower image's opacity.
9. Copy background of main game and layer it behind the dissapearing image(s)

#### Transitioning from cutscene to scene with gameplay logic. 

1. create a scene changer gameobject with a scene changer c# script component.
2. Open the scenechanger class, make sure it's using Unity.Engine.SceneManagement
3. Create a float variable that will be used to determine the amount of time the cut scene has before transitioning back to the gameplay scene. 
4. Create an if statement within the update method of the class which tracks when the transition time reaches zero and as a result, loads the gameplay scene. 


### Activity 2

Built in class today, I was able to use timeline to make a start of game cutscene and two transitions for when the player reaches the end of their dialogue and is sent to a end game scene. for my starting scene I made it transition fade to the game's enviornment scene 
and using a scene changer script I coded so that when the scene ran for a certain amount of time it would then load to the scene that stores all my games' gameplay. 


## W6

### Activity 1

#### Playtest Goals and Current Progress
Since milestone 1, my current build has two new scenes: a start game scene with a start button that leads into an opening cutscene and then transitions into gameplay. I have also added more official dialogue rather than placeholders. 
As for my playtest notes, I want to see if players enjoy the cutscenes, the art, and ask them questions about dialogue (how does this character make you feel?) Just to see if my narrative point is hitting the mark.

[Link to playtest build](https://kxcastilliano.itch.io/kalidescope-eyes-56)

#### Playtest Notes

- Players enjoyed the cutscene and it gave good context to the storyline of the game.
- Dialogue choices and mechanics ran smoothly. 
- Dialogue is well written and story seems interesting. 

### Activity 2

#### Question 1
Since all of the color values are decimals and scale from 0-1, that would mean when multiplying two decimal based numbers together the end result would be a smaller decimal. Smaller decimal numbers create darker numbers since they are closer to 0. 

#### Question 2

If we used Multiply for the alpha layers I'd assume it would make things more transparent given the logic where smaller numbers come out of multiplicatrion and the closer to zero it get's the more transparent it will be from a scale of 0-1.

#### Question 3

The shader grabs the UV values from the Shiba textures mesh values. 

#### Question 4

Coming from someone who is an artist and is familair with this values such as Multiply and Overlay I do think seeing it break down mathmatically and seeing these value happen and process in code is interesting and am curious to learn more about it!


## W7 

### Devlog Questions: Shader Activity

1. In our vertex color shader in step 2, the color from the vertex color node is from the color data that can be defined through the meshes vertex.

2. the color of our shiba in step 3 is blended  at the edges of different regions of colors since the data is tracking the mesh's surgace normals and given the dats o the mesh's x,y,z it tracks and converts it into it's corresponding colors depending on the axis. 

3. The coloring of th vertex color is less detailed due to the constraints that come with only utulizing the meshes vertex information. It only knocks down 3 colors for it's three surface normal axis which means the shiba is only gonna be colored with three colors. A good usage for vertex colors could be simple game objects and textures such as fire or water. 

4. Based on the coloring it appear's that the shiba's normals are having it so that the lighting is having the shiba lit backwards, when it's values should have it so that the outer surface of the shiba are brighter.

5. We can use the dot poduct and lighting system of vertex nodes for debugging as we are able to verify that the lighting and shadinf of certain gameobjects is facing the same direction or ideal direction we want it to be on. 

6. The light is pointing towards the shiba however it's polygons that are facing the light are dark when they should be light. 

7. We had sent the Blend mode to Additive in order to make the fire have that translucent glow to it. 

## W8

### Activity 1: Playtest

#### Pre-playtest
Since milestone 2, I wasn't able to do much towards the progression of the game coding wise, There has been new dialogue written but hsnt been added to the gameloop. The game's start game scene also uses a subtle shader graph. 
[Here is a link to the playtesting build](https://kxcastilliano.itch.io/kaleidoscope-eyes-520-build)

#### Playtesting goals
My playtesitng goals for this session:
Should there be a visual indicator that shows players that they are out of a cutscene and can now play through dialogue?
Is there enough routes/ choice sequences and endings to the game or should there be more progression?
Thoughts on the current cutscene/story.

#### Playtesting notes 




