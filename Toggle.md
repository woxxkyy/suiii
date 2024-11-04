package com.example.toggle;
import android.app.Activity;
import android.os.Bundle;
import android.widget.ImageView;
import android.view.View.OnClickListener;
import android.view.View;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final ImageView first_image = (ImageView)this.findViewById(R.id.first_image);
        final ImageView second_image = (ImageView)this.findViewById(R.id.second_image);
        first_image.setOnClickListener(new OnClickListener(){
            public void onClick(View view) {
                second_image.setVisibility(View.VISIBLE);
                view.setVisibility(View.GONE);
            }
        });
        second_image.setOnClickListener(new OnClickListener(){
            public void onClick(View view) {
                first_image.setVisibility(View.VISIBLE);
                view.setVisibility(View.GONE);
            }
        });
    }
}





<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <ImageView
        android:id="@+id/first_image"
        android:src = "@drawable/a"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:scaleType="fitXY" />
    <ImageView
        android:id="@+id/second_image"
        android:src = "@drawable/b"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:scaleType="fitXY" />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Click the image to switch"
        android:layout_gravity="center_horizontal|bottom"
        android:padding="5dip"
        android:textColor="#ffffff"
        android:textStyle="bold"
        android:background="#333333"
        android:layout_marginBottom="10dip" />

</FrameLayout>