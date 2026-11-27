# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Design the layout using activity_main.xml.

Step 3: Add an ImageView to display the image and add buttons for each animation (Move, Blink, Fade, Clockwise, Zoom, Slide).

Step 4: Import the image into the drawable folder.

Step 5: Create animation XML files under res/anim/ for each animation type such as blink, fade, move, rotate, slide and zoom.

Step 6: Type the Java program in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: Kowshika R
Registeration Number : 212224220049
*/
```

## main_avtivity.java

```
package com.example.animationapplication;

import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.Button;
import android.widget.ImageView;

public class MainActivity extends Activity {

    ImageView imageView;

    Button btnMove;
    Button btnBlink;
    Button btnFade;
    Button btnClockwise;
    Button btnZoom;
    Button btnSlide;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        imageView = findViewById(R.id.imageView);

        btnMove = findViewById(R.id.btnMove);
        btnBlink = findViewById(R.id.btnBlink);
        btnFade = findViewById(R.id.btnFade);
        btnClockwise = findViewById(R.id.btnClockwise);
        btnZoom = findViewById(R.id.btnZoom);
        btnSlide = findViewById(R.id.btnSlide);

        btnMove.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.move);
                imageView.startAnimation(animation);
            }
        });

        btnBlink.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.blink);
                imageView.startAnimation(animation);
            }
        });

        btnFade.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.fade);
                imageView.startAnimation(animation);
            }
        });

        btnClockwise.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.clockwise);
                imageView.startAnimation(animation);
            }
        });

        btnZoom.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.zoom);
                imageView.startAnimation(animation);
            }
        });

        btnSlide.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Animation animation =
                        AnimationUtils.loadAnimation(MainActivity.this, R.anim.slide);
                imageView.startAnimation(animation);
            }
        });
    }
}
```
## activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:src="@drawable/img"
        android:scaleType="centerInside"
        android:contentDescription="Animated Image" />

    <Button
        android:id="@+id/btnMove"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Move" />

    <Button
        android:id="@+id/btnBlink"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Blink" />

    <Button
        android:id="@+id/btnFade"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Fade" />

    <Button
        android:id="@+id/btnClockwise"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Clockwise" />

    <Button
        android:id="@+id/btnZoom"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Zoom" />

    <Button
        android:id="@+id/btnSlide"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Slide" />

</LinearLayout>
```
## fade.xml

```
<?xml version="1.0" encoding="utf-8"?>
<alpha xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromAlpha="1.0"
    android:toAlpha="0.0"
    android:duration="2000" />
```
## blink.xml

```
<?xml version="1.0" encoding="utf-8"?>
<alpha xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromAlpha="1.0"
    android:toAlpha="0.0"
    android:duration="500"
    android:repeatMode="reverse"
    android:repeatCount="5" />
```
## move.xml

```
<?xml version="1.0" encoding="utf-8"?>
<translate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXDelta="0"
    android:toXDelta="300"
    android:fromYDelta="0"
    android:toYDelta="0"
    android:duration="1000" />
```

## clockwise.xml

```
<?xml version="1.0" encoding="utf-8"?>
<rotate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromDegrees="0"
    android:toDegrees="360"
    android:pivotX="50%"
    android:pivotY="50%"
    android:duration="1000" />
```
## slide.xml

```
<?xml version="1.0" encoding="utf-8"?>
<translate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXDelta="-300"
    android:toXDelta="0"
    android:fromYDelta="0"
    android:toYDelta="0"
    android:duration="1000" />
```

## zoom.xml

```
<?xml version="1.0" encoding="utf-8"?>
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXScale="1.0"
    android:toXScale="2.0"
    android:fromYScale="1.0"
    android:toYScale="2.0"
    android:pivotX="50%"
    android:pivotY="50%"
    android:duration="1000" />
```

## OUTPUT

<img width="1917" height="1140" alt="image" src="https://github.com/user-attachments/assets/00b13508-2079-46fa-9e5e-04e9597f5a5c" />

<img width="1912" height="1140" alt="image" src="https://github.com/user-attachments/assets/98da6bb6-d0c7-4eb3-8cf5-1c91ba937298" />

<img width="1917" height="1137" alt="image" src="https://github.com/user-attachments/assets/78f494b5-67bc-4340-80a8-283da37b2704" />

<img width="1917" height="1140" alt="image" src="https://github.com/user-attachments/assets/4274a09f-0743-4bcc-9b56-5576800efab6" />

<img width="1917" height="1140" alt="image" src="https://github.com/user-attachments/assets/be4df93b-91e8-40b8-abce-cc8b130b45fa" />

<img width="1907" height="1140" alt="image" src="https://github.com/user-attachments/assets/72e7badc-a226-4847-b888-5271ef3320d9" />


## RESULT

Thus,the experiment Implementation of Animation application using android studio executed successfully.
