# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.
## AIM:
To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.
## EQUIPMENTS REQUIRED:

Latest Version Android Studio
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
/*
Program to print the text “Hello World”.
Developed by: NIRANJANA DEVI S
Registeration Number : 212221220036
*/
```
Activity_main.xml:
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent" tools:context=".MainActivity">
~~~
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="40dp"
    android:text="Hello World!"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"#
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
~~~
</androidx.constraintlayout.widget.ConstraintLayout>
## MainActivity.java:
package com.example.myapplication;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle; import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
~~~
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    Toast toast = Toast.makeText(getApplicationContext(), "onCreate Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onStart() {
    super.onStart();
    Toast toast = Toast.makeText(getApplicationContext(), "onStart Called", Toast.LENGTH_LONG);
    toast.show();
}
@Override
protected void onRestart() {
    super.onRestart();
    Toast toast = Toast.makeText(getApplicationContext(), "onRestart Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onPause() {
    super.onPause();
    Toast toast = Toast.makeText(getApplicationContext(), "onPause Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onResume() {
    super.onResume();
    Toast toast = Toast.makeText(getApplicationContext(), "onResume Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onStop() {
    super.onStop();
    Toast toast = Toast.makeText(getApplicationContext(), "onStop Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onDestroy() {
    super.onDestroy();
    Toast toast = Toast.makeText(getApplicationContext(), "onDestroy Called", Toast.LENGTH_LONG);
    toast.show();
}
}
~~~
## OUTPUT
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/b9d21b15-1b51-48f9-a1c5-f86f3519aed9)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/6ba4e38a-e8f3-4937-9c04-fcf4dbabd961)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/52524ec7-b364-40ce-b1a6-c05900058e36)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/746bdd6e-8d19-45a2-9e12-85a61cada556)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/9e039748-c381-4efd-8b66-1ae87a442df2)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/0efe15b2-bedf-4807-aff3-f57032a1044d)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/77f103d1-1316-4e95-bdcc-10a06a7bc617)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/5e3c4613-7713-49e7-8efe-565423818830)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/c65b967f-2d6a-44b1-8a74-adb5f832f573)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/1a256e86-8e5e-40c5-b095-6aff7df6b68a)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/f208dfb7-fd86-4e64-888f-8a57ef50120c)
![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/1933f265-7071-45cb-b0b1-b98c4ae3f592)

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
