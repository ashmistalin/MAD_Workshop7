# MAD_workshop7

## Develop an android application while closing app or pressing button show alert or warning message in android studio using alert or prompt dialog box.

## AIM:
To develop an android application while closing app or pressing button show alert or warning message in android studio using alert or prompt dialog box.
```
/*
Submitted by: ASHMI S
Register number: 212221040021
*/
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Press the back button of your phone."
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java:
```
package com.example.alert;

import android.content.DialogInterface;
import android.os.Bundle;
import androidx.appcompat.app.AlertDialog;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    @Override
    public void onBackPressed() {
        AlertDialog.Builder builder = new AlertDialog.Builder(MainActivity.this);
        builder.setMessage("Do you want to exit ?");
        builder.setTitle("Alert !");
        builder.setCancelable(false);
        builder.setPositiveButton("Yes", (DialogInterface.OnClickListener) (dialog, which) -> {
            finish();
        });
        builder.setNegativeButton("No", (DialogInterface.OnClickListener) (dialog, which) -> {
            dialog.cancel();
        });
        AlertDialog alertDialog = builder.create();
        alertDialog.show();
    }
}

```

## OUTPUT:
![Screenshot (358)](https://github.com/ashmistalin/MAD--Workshop5/assets/103128410/f1f727aa-47f4-4634-87d6-4c2b8f3e0179)
![Screenshot (359)](https://github.com/ashmistalin/MAD--Workshop5/assets/103128410/55acfc53-8fba-41cd-9735-6375f007f0a5)


## RESULT:
Thus an android application while closing app or pressing button show alert or warning message in android studio using alert or prompt dialog box is developed.
 
