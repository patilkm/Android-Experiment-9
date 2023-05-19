# Android-Experiment-9
Design a mobile application for media player.
Procedure:

Step 1: Create a New Project in Android Studio Step 1: Open a new android project
After opening the Android Studio you have to create a new project using the Empty Activity with language as Java and give your project a unique name as you wish but don’t forget to keep the first alphabet capital.
1.	Go to the top left corner and then hit File->New->New Project as shown in the following screenshot.
2.	Select Empty Activity as shown in the following screenshot.
3.	Give your project a name, choose java and use lower level API so that your app can run on older version of android phones
Step 2: Designing the User Interface of the app
Step 3: Adding the music file to our app
Add the mp3 file to the raw folder. You can reach there by:
app-> res-> raw
If there is no raw folder, then create it by right-clicking on res directory then:
res-> new-> directory
Name the newly created directory as raw and add all the audio files in this folder. Drag and drop files here is not allowed. You have to copy your source file, then right-click on the raw directory and click paste. Use “show in explorer” (if you are using windows) to go to that particular file. Make sure that the new name contains all small alphabets. The only valid characters are (a-z and 0-9 and _ )
Step 4: Let’s code the functionality of our App
1.	Make a object of MediaPlayer class named music. It is an inbuilt class in android package. All the properties of the MediaPlayer class can be used by this music object:
MediaPlayer music
2.	We will add our music file to this newly created object by using create function :
music = MediaPlayer.create(this, R.raw.sound);
Please note that there is no need to add .mp3 or .wav or whatever filetype you are using. Just add the name of the file. (I have named my file as sound.mp3 so used R.raw.sound)
3.	MediaPlayer class has an inbuilt function called start we will use this function for play button. It will start the song.
public void playSong(View v){
music.start();
}
4.	For pause button we will use the inbuilt function pause. This will pause the song.
public void pauseSong(View v) {
mp.pause();
}
5.	For stop button we will use the inbuilt stop function. This function also deletes the object (music), so we create a new object with the same name.

public void stopSong(View v) {
mp.stop();
}
music = MediaPlayer.create(this, R.raw.sound);
Note: The audio files are stored in the app, so make sure small files are added
The complete Java code: MainActivity.java file
Step 5: Let’s Run our app
Click the “Run” button at the Toolbar at the top to run our code.
 
