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
