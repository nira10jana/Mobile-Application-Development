# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as implicit inetent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: NIRANJANA DEVI S
Registeration Number : 212221220036
*/
```

Activity_main.xml:

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

~~~

xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools"

android:layout_width="match_parent"

android:layout_height="match_parent"

tools:context=".MainActivity">

<EditText
    android:id="@+id/editTextTextPersonName"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="60dp"
    android:layout_marginTop="284dp"
    android:ems="10"
    android:inputType="textPersonName"
    android:text=""
    android:textSize="25sp"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/button"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginBottom="128dp"
    android:onClick="Showdtag"
    android:text="Factorial"
    android:textSize="25sp"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.506"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/editTextTextPersonName"
    app:layout_constraintVertical_bias="0.831" />

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginBottom="52dp"
    android:text="Enter a number:"
    android:textSize="25sp"
    app:layout_constraintBottom_toTopOf="@+id/editTextTextPersonName"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.497"
    app:layout_constraintStart_toStartOf="parent" />

<TextView
    android:id="@+id/textView4"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Factorial of a Number"
    android:textSize="30sp"
    app:layout_constraintBottom_toTopOf="@+id/textView"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.52"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintVertical_bias="0.62" />

~~~

</androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity.java:

package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.EditText;

public class MainActivity extends AppCompatActivity { EditText ed1; Button res;

~~~

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    ed1 = findViewById(R.id.editTextTextPersonName);
    res = findViewById(R.id.button);
    res.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            int num = Integer.parseInt(ed1.getText().toString());
            int factorial = calculateFactorial(num);
            Intent intent = new Intent(getApplicationContext(), MainActivity2.class);
            intent.putExtra("key", factorial);
            startActivity(intent);
        }
    }
}

private int calculateFactorial(int number) {
    int factorial = 1;
    for (int i = 1; i <= number; i++) {
        factorial *= i;
    }
    return factorial;
}

~~~

}

## Activity_main2.xml:

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

~~~
xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools"

android:layout_width="match_parent"

android:layout_height="match_parent"

tools:context=".MainActivity2">

<TextView
    android:id="@+id/textView3"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text=""
    android:textSize="40dp"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.464"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
<TextView
    android:id="@+id/textView5"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Result:"
    android:textSize="40dp"
    app:layout_constraintBottom_toTopOf="@+id/textView3"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.465"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintVertical_bias="0.825" />

~~~
</androidx.constraintlayout.widget.ConstraintLayout>

## MainActivity2.java:

package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent; import android.os.Bundle; import android.widget.TextView;

public class MainActivity2 extends AppCompatActivity { TextView getdata;

~~~

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main2);
    getdata = findViewById(R.id.textView3);
    Intent intent = getIntent();
    int data = intent.getIntExtra("key",0);
    getdata.setText(Integer.toString(data));
}
~~~

}

## OUTPUT

![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/a5cd5ef6-e196-4c54-b434-0cdb32cb7a25)

![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/9f02a4cb-06b4-4de9-8bb4-91a84a087a7a)

![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/cc5e2cc6-d432-43f6-a641-d71eb841da34)

![image](https://github.com/nira10jana/Mobile-Application-Development/assets/141748873/0a24cb75-0909-4505-af68-fa94619175b3)


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


