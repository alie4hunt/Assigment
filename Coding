##calculator.java
package com.inti.student.calculator;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.webkit.WebView;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

public class calculator extends AppCompatActivity {

    Button sum, subtract, multiply, divide, remainder, clear;
    TextView answer;
    EditText num1, num2;
    private int no1, no2, result;
    private double a, b, resultD;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_calculator);

        //Finding views
        sum = findViewById(R.id.sum);
        subtract = findViewById(R.id.subtract);
        multiply = findViewById(R.id.multiply);
        divide = findViewById(R.id.divide);
        remainder = findViewById(R.id.remainder);
        clear = findViewById(R.id.clear);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);

        answer = findViewById(R.id.answer);


        sum.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Add();
            }
        });

        subtract.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Sub();
            }
        });

        multiply.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Mult();
            }
        });

        divide.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Div();
            }
        });

        remainder.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Rem();
            }
        });

        clear.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Clr();
            }
        });


    }

     private void Add() {
        if (num1.getText().toString().length() !=0 && num2.getText().toString().length() !=0) {
             if (num1.getText().toString().contains(".") || num2.getText().toString().contains(".")) {
                a = Double.parseDouble(num1.getText().toString());
                b = Double.parseDouble(num2.getText().toString());
                resultD = a + b;
                answer.setText(String.valueOf(resultD));
            } else {
                no1 = Integer.parseInt(num1.getText().toString());
                no2 = Integer.parseInt(num2.getText().toString());
                result = no1 + no2;
                answer.setText(String.valueOf(result));
            }
        } else {
            Toast errorToast = Toast.makeText(calculator.this, "Please make sure all column is filled up!!!", Toast.LENGTH_SHORT);
            errorToast.show();
        }
    }


    private void Sub() {
        if (num1.getText().toString().length() !=0 && num2.getText().toString().length() !=0) {
             if (num1.getText().toString().contains(".") || num2.getText().toString().contains(".")) {
                a = Double.parseDouble(num1.getText().toString());
                b = Double.parseDouble(num2.getText().toString());
                resultD = a - b;
                answer.setText(String.valueOf(resultD));
            } else {
                no1 = Integer.parseInt(num1.getText().toString());
                no2 = Integer.parseInt(num2.getText().toString());
                result = no1 - no2;
                answer.setText(String.valueOf(result));
            }
        } else {
            Toast errorToast = Toast.makeText(calculator.this, "Please make sure all column is filled up!!!", Toast.LENGTH_SHORT);
            errorToast.show();
        }
    }


    private void Mult() {
        if (num1.getText().toString().length() !=0 && num2.getText().toString().length() !=0) {
            if (num1.getText().toString().contains(".") || num2.getText().toString().contains(".")) {
                a = Double.parseDouble(num1.getText().toString());
                b = Double.parseDouble(num2.getText().toString());
                resultD = a * b;
                answer.setText(String.valueOf(resultD));
            } else {
                no1 = Integer.parseInt(num1.getText().toString());
                no2 = Integer.parseInt(num2.getText().toString());
                result = no1 * no2;
                answer.setText(String.valueOf(result));
            }
        } else {
            Toast errorToast = Toast.makeText(calculator.this, "Please make sure all column is filled up!!!", Toast.LENGTH_SHORT);
            errorToast.show();
        }
    }

    private void Div() {
        if (num1.getText().toString().length() !=0 && num2.getText().toString().length() !=0) {
            if (num1.getText().toString().contains(".") || num2.getText().toString().contains(".")) {
                a = Double.parseDouble(num1.getText().toString());
                b = Double.parseDouble(num2.getText().toString());
                resultD = a / b;
                answer.setText(String.valueOf(resultD));
            } else {
                no1 = Integer.parseInt(num1.getText().toString());
                no2 = Integer.parseInt(num2.getText().toString());
                result = no1 / no2;
                answer.setText(String.valueOf(result));
            }
        } else {
            Toast errorToast = Toast.makeText(calculator.this, "Please make sure all column is filled up!!!", Toast.LENGTH_SHORT);
            errorToast.show();
        }
    }

    private void Rem() {
        if (num1.getText().toString().length() !=0 && num2.getText().toString().length() !=0) {
            if (num1.getText().toString().contains(".") || num2.getText().toString().contains(".")) {
                a = Double.parseDouble(num1.getText().toString());
                b = Double.parseDouble(num2.getText().toString());
                resultD = a % b;
                answer.setText(String.valueOf(resultD));
            } else {
                no1 = Integer.parseInt(num1.getText().toString());
                no2 = Integer.parseInt(num2.getText().toString());
                result = no1 % no2;
                answer.setText(String.valueOf(result));
            }
        } else {
            Toast errorToast = Toast.makeText(calculator.this, "Please make sure all column is filled up!!!", Toast.LENGTH_SHORT);
            errorToast.show();
        }
    }

    public void Clr() {
        if (num1.getText().toString().length() >= 1 && num2.getText().toString().length() >= 1) {
            num1.setText("");
            num2.setText("");
            answer.setText("");

        }
    }
}
activity_calculator.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
                xmlns:app="http://schemas.android.com/apk/res-auto"
                xmlns:tools="http://schemas.android.com/tools"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:paddingLeft="16dp"
                android:paddingTop="16dp"
                android:paddingRight="16dp"
                android:paddingBottom="16dp"
                tools:context=".calculator">




    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="10dp"
        android:ems="10"
        android:hint="Number1"
        android:inputType="number|numberDecimal|numberSigned"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="62dp"
        android:ems="10"
        android:hint="Number2"
        android:inputType="number|numberDecimal|numberSigned"/>

    <!--Created By Ashim -->

    <Button
        android:id="@+id/sum"
        android:layout_width="353dp"
        android:layout_height="wrap_content"
        android:layout_above="@+id/subtract"
        android:layout_marginBottom="0dp"
        android:text="Sum +"
        android:textSize="25sp"/>

    <Button
        android:id="@+id/subtract"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_marginBottom="160dp"
        android:text="Subtract -"
        android:textSize="25sp"/>

    <Button
        android:id="@+id/multiply"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/subtract"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="-160dp"
        android:text="Multiply x"
        android:textSize="25sp"/>

    <Button
        android:id="@+id/remainder"
        android:layout_width="354dp"
        android:layout_height="53dp"
        android:layout_below="@+id/divide"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="-7dp"
        android:text="Remainder %"
        android:textSize="25sp"/>

    <Button
        android:id="@+id/divide"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/multiply"
        android:layout_centerHorizontal="true"
        android:layout_marginBottom="7dp"
        android:text="Divide /"
        android:textSize="25sp"/>

    <Button
        android:id="@+id/clear"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/answer"
        android:layout_marginTop="-313dp"
        android:layout_marginEnd="34dp"
        android:layout_marginRight="34dp"
        android:text="Clear"/>

    <TextView
        android:id="@+id/answer"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:layout_marginBottom="313dp"
        android:textSize="30sp"/>


</RelativeLayout>

