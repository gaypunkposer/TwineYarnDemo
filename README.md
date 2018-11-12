# TwineYarnDemo
A Unity project with a Twine story ported to Yarn Spinner

# Porting a Twine story to Yarn
This involves a few steps, and I really want to automate this process in the future.  
1. Convert your Twine story to Twee  
  This involves setting http://www.maximumverbosity.net/twine/Entweedle/ as your Story Format  
2. Copy the Twee code to a .txt file  
  Once Entweedle is your Story Format, hit play. Copy the output from the popup window into a new .txt file. Pressing "Publish to File"
  creates an HTML document with the Twee code inside, which is not what we want.
3. Open your new .txt file with Twee code in Yarn  
  Your nodes won't be in the right position, but all the links should be there.  
4. Make adjustments as needed.  
  If statements are slightly differnt in Yarn, and Yarn has a feature called "shortcuts" that lets you present a dialogue option,
  a response, and continue along a set story. Normally in Twine this would require multiple nodes.
5. Save as Yarn.  
  Save as a .yarn.txt file in your Unity assets folder
6. Load the Dialogue prefab from Dialogue.unitypackage into your Unity scene.  
  The basic prefab includes three possible responses, a speaker text object, and a dialogue text object, along with the script necessary to run it.
7. Add your dialogue to the Dialogue Runner object in the editor, or add it later using DialogueRunner.AddScipt(your script).  
8. Call Start() or Start(string node) on the DialogueRunner object to start the dialogue.
