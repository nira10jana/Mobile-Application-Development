# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.
## AIM:
To create and design an android application that draws basic graphical primitives on the screen using Android Studio.
## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)
## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as “graphical″ and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Draw basic object details give in MainActivity file.
Step 7: Save and run the application.
## PROGRAM:
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by:NIRANJANA DEVI .S
Registeration Number :212221220036
*/
## Activity_main.xml:
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
~~~
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
<ImageView
    android:id="@+id/imageView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    tools:srcCompat="@tools:sample/avatars" />
~~~
## MainActivity.java:
package com.example.shapes;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;
public class MainActivity extends AppCompatActivity {
~~~
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
try {
        Bitmap bitmap = Bitmap.createBitmap(720, 1280, Bitmap.Config.ARGB_8888);
        ImageView imageView = findViewById(R.id.imageView);
        imageView.setBackground(new BitmapDrawable(getResources(), bitmap));
        Canvas canvas = new Canvas(bitmap);
        Paint paint = new Paint();
        paint.setColor(Color.BLUE);
        paint.setTextSize(50);
        canvas.drawText("Rectangle", 420, 150, paint);
        canvas.drawRect(400, 200, 650, 700, paint);
        canvas.drawText("Circle", 120, 150, paint);
        canvas.drawCircle(200, 350, 150, paint);
        canvas.drawText("Square", 120, 800, paint);
        canvas.drawRect(50, 850, 350, 1150, paint);
        canvas.drawText("Line", 420, 800, paint);
        canvas.drawLine(520, 850, 520, 1150, paint);
    } catch (Exception e) {
        e.printStackTrace();
    }
}
~~~
## OUTPUT
![ex11 4](https://github.com/Aishwarya-TM/Mobile-Application-Development/assets/127846109/815b211f-e2d7-4151-97e6-03818a786c6c)
![ex11 5](https://github.com/Aishwarya-TM/Mobile-Application-Development/assets/127846109/2b5e4f0a-9162-4551-ba5c-1fa17adeea9d)
## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
