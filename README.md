package com.example.test41;
import android.annotation.SuppressLint;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;
public class MainActivity extends AppCompatActivity {
 Button btn2;
 @SuppressLint("MissingInflatedId")
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 btn2=findViewById(R.id.button1);
 String text=getIntent().getStringExtra("data");
 btn2.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 Intent i =new Intent(MainActivity.this, MainActivity2.class);
 startActivity(i);
 }
 });
 }



 package com.example.test41;
import android.annotation.SuppressLint;
import android.content.Intent;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;
public class MainActivity2 extends AppCompatActivity {
 TextView ed1,ed2,ed3,ed4;
 String tag="event";
 Button btn1;
 @SuppressLint("MissingInflatedId")
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main2);
 Log.d(tag,"hello");
 ed1=findViewById(R.id.editTextText1);
 ed2=findViewById(R.id.editTextText2);
 ed3=findViewById(R.id.editTextText3);
 ed4=findViewById(R.id.editTextText4);
 btn1=findViewById(R.id.button2);
 btn1.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 Intent i=new Intent(MainActivity2.this, MainActivity3.class);
 String text1=ed1.getText().toString();
 i.putExtra("data1",text1);
 String text2=ed2.getText().toString();
 i.putExtra("data2",text2);
 String text3=ed3.getText().toString();
 i.putExtra("data3",text3);
 String text4=ed4.getText().toString();
 i.putExtra("data4",text4);
 startActivity(i);
 }



 MainActivity3.java
package com.example.test41;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;
public class MainActivity3 extends AppCompatActivity {
 TextView ed1,ed2,ed3,ed4;
 Button btn2;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main4);
 ed1=findViewById(R.id.textview1);
 ed2=findViewById(R.id.textview2);
 ed3=findViewById(R.id.textview3);
 ed4=findViewById(R.id.textview4);
 btn2=findViewById(R.id.button2);
 String text1=getIntent().getStringExtra("data1");
 ed1.setText(text1);
 String text2=getIntent().getStringExtra("data2");
 ed2.setText(text2);
 String text3=getIntent().getStringExtra("data3");
 ed3.setText(text3);
 String text4=getIntent().getStringExtra("data4");
 ed4.setText(text4);
 btn2.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 Intent i =new Intent(MainActivity3.this,MainActivity.class);
 startActivity(i);
 }
 });
MAD LAB
 }
