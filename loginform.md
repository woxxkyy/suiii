package com.example.loginform;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText un =(EditText) findViewById(R.id.username);
        EditText pw =(EditText) findViewById(R.id.password);
        Button btn =(Button) findViewById(R.id.idBtnLogin);
        btn.setOnClickListener(view -> {
            String uname = un.getText().toString();
            String passwd = pw.getText().toString();
            if(uname.equals("user") && passwd.equals("123")){
                Toast.makeText(this,"Login Success",Toast.LENGTH_SHORT).show();
            }else{
                Toast.makeText(this,"invalid username/password",Toast.LENGTH_SHORT).show();
            }
        });
    }
}



<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <!-- Title TextView -->
    <TextView
        android:id="@+id/login"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:gravity="center_horizontal"
        android:padding="5dp"
        android:text="Login Form"
        android:textAlignment="center"
        android:textColor="@android:color/black"
        android:textSize="18sp" />

    <!-- Username Label -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Username"
        android:layout_below="@id/login"
        android:layout_marginTop="30dp"
        android:layout_marginStart="13dp"/>

    <!-- Username EditText -->
    <EditText
        android:id="@+id/username"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/login"
        android:layout_marginTop="50dp"
        android:layout_marginStart="10dp"
        android:layout_marginEnd="10dp"
        android:hint="Enter Username"
        android:inputType="textEmailAddress" />

    <!-- Password Label -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Password"
        android:layout_below="@id/username"
        android:layout_marginTop="20dp"
        android:layout_marginStart="13dp" />

    <!-- Password EditText -->
    <EditText
        android:id="@+id/password"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/username"
        android:layout_marginTop="50dp"
        android:layout_marginStart="10dp"
        android:layout_marginEnd="10dp"
        android:hint="Enter Password"
        android:inputType="textPassword" />

    <!-- Login Button -->
    <Button
        android:id="@+id/idBtnLogin"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/password"
        android:layout_marginTop="20dp"
        android:layout_marginStart="10dp"
        android:layout_marginEnd="10dp"
        android:text="Login" />
</RelativeLayout>
