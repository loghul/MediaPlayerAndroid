### EX NO : 03
### DATE  : 11/10/22
# <p align="center">  To develop a simple application to play and control the audio file in android studio.
 </p>

## AIM:

To Develop a simple application to play and control the audio file in android studio.


## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Developed by: Loghul M
Registeration Number : 212220230029

```

activityMain.xml:

```java


<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="play"
        android:text="Play"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.442"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.281" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="248dp"
        android:layout_marginEnd="180dp"
        android:onClick="pause"
        android:text="Pause"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="stop"
        android:text="Stop"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.442"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.584" />
</androidx.constraintlayout.widget.ConstraintLayout>

```
## MainActivity.java
```java
package com.example.mediaplayer;

import android.content.Context;
import android.media.MediaPlayer;
import android.os.Bundle;
import android.view.View;
import android.widget.Toast;


import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    MediaPlayer player;
    private Context context;
    private Object text;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    public void play(View v){
        if(player==null){
            player= MediaPlayer.create(this,R.raw.song);
            player.setOnCompletionListener(new MediaPlayer.OnCompletionListener(){
                public void onCompletion(MediaPlayer mp){
                    stopPlayer();
                }
            });
        }
        player.start();

    }
    public void pause(View v){
        if(player!=null){
            player.pause();
        }

    }
    public void stop(View v){
        stopPlayer();


    }
    private void stopPlayer(){
        if(player!=null){
            player.release();
            player=null;
            Toast.makeText(this,"MediaPlayer released",Toast.LENGTH_SHORT).show();

        }
    }
}


```
## OUTPUT
![Screenshot (8)](https://user-images.githubusercontent.com/78194419/195649246-a3c6624e-e43f-4bea-9625-4c98e04ddc16.png)
![Screenshot (7)](https://user-images.githubusercontent.com/78194419/195649279-4e3e28a0-263f-45ca-b0f5-91827deefaa8.png)


## RESULT
Thus a Simple Android Application create a dtatabase table and to display the database table  using SQLite Database in Android Studio is developed and executed..

