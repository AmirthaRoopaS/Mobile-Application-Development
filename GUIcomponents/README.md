# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:


## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by:Amirtha Roopa.S
Registeration Number :212221220005
*/
```
## activity main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<Button
  android:id="@+id/colbut"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginStart="128dp"
  android:layout_marginTop="120dp"
  android:backgroundTint="#FFC107"
  android:text="Change Color"
  app:layout_constraintStart_toStartOf="parent"
  app:layout_constraintTop_toTopOf="parent" />

<Button
  android:id="@+id/fonbut"
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:layout_marginStart="132dp"
  android:layout_marginTop="48dp"
  android:backgroundTint="#FF5722"
  android:text="Change Font"
  app:layout_constraintStart_toStartOf="parent"
  app:layout_constraintTop_toBottomOf="@+id/colbut" />

<TextView
android:id="@+id/textView"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_marginStart="48dp"
android:layout_marginTop="152dp"
android:text="PRIME PLAYS"
android:textSize="40dp"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/fonbut" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.guicomps;
import androidx.appcompat.app.AppCompatActivity;
import android.content.res.AssetManager;
import android.graphics.Color;
import android.graphics.Typeface;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import java.io.IOException;
import java.io.InputStream;

public class MainActivity extends AppCompatActivity implements View.OnClickListener
{
 private TextView textView;
private Button colorButton;
private Button fontButton;
@Override
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(savedInstanceState);
  setContentView(R.layout.activity_main);
  textView = findViewById(R.id.textView);
  colorButton = findViewById(R.id.colbut);
  fontButton = findViewById(R.id.fonbut);
  colorButton.setOnClickListener(this);
  fontButton.setOnClickListener(this);
}

@Override
public void onClick(View view) {
  switch (view.getId()) {
    case R.id.colbut:
      changeTextColor();
      break;
    case R.id.fonbut:
      changeFont();
      break;
  }
}

private void changeTextColor() {
  int randomColor = generateRandomColor();
  textView.setTextColor(randomColor);
}

private void changeFont() {
  Typeface newFont = Typeface.createFromAsset(getAssets(), "font/pacifico.ttf");
  textView.setTypeface(newFont);
}

private int generateRandomColor() {
  int red = (int) (Math.random() * 256);
  int green = (int) (Math.random() * 256);
  int blue = (int) (Math.random() * 256);
  return Color.rgb(red, green, blue);
  }
}
```

## OUTPUT
![image](https://github.com/suryacse05/Mobile-Application-Development/assets/143496311/60441b65-7872-4bc1-a595-dab28c93adab)
![image](https://github.com/suryacse05/Mobile-Application-Development/assets/143496311/5d22f7b3-5d3c-42b3-b3b3-61f3b748697b)






## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


