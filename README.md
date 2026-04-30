# GDIM 33 In-Class Activities
## W1
### Activity 1
1. https://docs.google.com/drawings/d/1Bz43Q08DGFOCgmofemXLwSxpZa4YqZLi2pbqFyB1qss/edit?usp=sharing
2. 
    (1) I love cities and buildings. I also love Japanese culture.
    (2) I cannot write this section because I was absent.
    (3) I cannot write this section because I was absent.
    
### Activity 2
(1) Papers, please-like
(2) A player works as a customs officer at an international airport in a fictional country. Travelers arrive one by one with passports, customs declaration forms, and luggage. The player must inspect each traveler, compare their documents with their appearance and baggage scan, and identify suspicious or anomalous traits before making a decision.
(3) https://docs.google.com/drawings/d/1NhbZnd_Kp8Ws2vqgfMxpA9pnqVoGAwDLbI3lQ5wfBoE/edit?usp=sharing


## W2
Write your W2 Devlog here.

Continue adding additional headers below this one for future weeks and future activities.


## W3
### Activity 1
https://drive.google.com/file/d/1tpfWW5tAJHiwwRU3NEbRoLNp9CLIksdd/view?usp=sharing

### Activity 2
1. Saving the event name as a Scene variable makes the graph easier to manage. If I want to change the event name later, I only need to change it in one place.
2. Debug.Log helped me check if my click event was working before the full state change worked correctly. When I saw the message in the Console, I knew that the graph was running at that step.
3. Yes, I think it is relevant because my game may need different player controls in different situations. For example, the player may move during gameplay, but use the mouse cursor during UI or dialogue.
4. Yes, the concept of game state is relevant to my Vertical Slice. My game can have different modes, such as checking documents, talking to characters, and showing UI, so changing states will help organize the gameplay.

## W4
### Activity 1
Playtest team members: beiduo jin, Thomas Sun
What is playable right now: conduct customs inspection for one person
Playtesting goal: conduct customs inspections for five people
Playtesting note: since the team members didn't understand how to play, it looks like a tutorial will be necessary.

### Activity 2
1. Yes, I think a writer could add more dialogue without writing code after the system is already set up by a programmer. The writer can create new dialogue nodes, write lines, and connect reply options in the Inspector. Because the dialogue content is stored as data, the writer does not need to change the actual system code unless they want new features.
2. do not think there is a strict limit to the total number of dialogue nodes. A writer could keep creating many nodes and linking them together. However, there are practical limits, such as how organized the project is and how many reply options can fit on the screen at one time. In this setup, the UI seems to support up to about four reply options at once before space becomes a problem.
3. The purpose of the “Regenerate Nodes” button is to update the Visual Scripting node library so Unity can recognize code and types as usable nodes. It helps Visual Scripting show the latest classes, methods, and data in the graph. Without regenerating nodes, newly added code or custom types might not appear correctly in Visual Scripting. This is especially important here because the activity says we need to manually add PlayerReplyW4 as a type before regenerating.


## W5
### Activity 1
1. Create the basic ScriptableObject data structure.
- I created a ScriptableObject type for traveler case data.
- This data object stores information such as the traveler name, passport information, declared items, actual luggage items, correct decision, and score result.
- Test: I created one case data asset in the Unity Project window and checked that I could edit the values in the Inspector.
2. Connect the ScriptableObject data to the case manager.
- I added a reference to the traveler case data in the case manager.
- Instead of writing all case information directly inside the script, the case manager now reads information from the ScriptableObject.
- Test: I pressed Play and checked that the traveler name, passport text, declaration text, and other case information appeared correctly on the UI.
3. Use the ScriptableObject data for gameplay decisions.
- I connected the correct decision and case information from the ScriptableObject to the approve/reject system.
- The game now checks the player’s decision against the case data instead of only using hard-coded values.
- Test: I tested both Approve and Reject and confirmed that the feedback and score changed based on the data stored in the ScriptableObject.
4. Prepare the system for more cases later.
- Since the case data is now separated from the main script, I can create more traveler cases by making more ScriptableObject assets.
- This should make it easier to add Case 2, Case 3, and future cases without rewriting the whole game manager.
- Test: I confirmed that the current case still works correctly after moving the case information into a ScriptableObject.

### Activity 2
I integrated ScriptableObjects into my vertical slice. Before this update, most of the case information was hard-coded in the case manager script. I changed the structure so that the traveler case data can be stored in a ScriptableObject asset. This includes information such as the traveler’s identity, passport information, declared items, actual luggage contents, and correct decision.I also connected this ScriptableObject data to the existing gameplay system. The UI now uses the data from the ScriptableObject, and the approve/reject decision can be checked based on that data. I tested the game in Unity, and the basic case still works correctly. This is useful because I can now add more traveler cases by creating new data assets instead of rewriting the main script every time.