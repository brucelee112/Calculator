# Calculator
private Button bt1;
    private Button bt2;
    private Button bt3;
    private Button bt4;
    private Button bt5;
    private Button bt6;
    private Button bt7;
    private Button bt8;
    private Button bt9;
    private Button bt10;
    private Button bt11;
    private Button bt12;
    private Button bt13;
    private Button bt14;
    private Button bt15;
    private Button bt16;
    private Button bt17;
    private Button bt18;
    private Button bt19;
    private EditText text;
    private float a;
    private float b;
    private String string="";
    private String string2="";
    private int id;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        bt1= (Button) findViewById(R.id.button);
        bt2= (Button) findViewById(R.id.button2);
        bt3= (Button) findViewById(R.id.button3);
        bt4= (Button) findViewById(R.id.button4);
        bt5= (Button) findViewById(R.id.button5);
        bt6= (Button) findViewById(R.id.button6);
        bt7= (Button) findViewById(R.id.button7);
        bt8= (Button) findViewById(R.id.button8);
        bt9= (Button) findViewById(R.id.button9);
        bt10= (Button) findViewById(R.id.button10);
        bt11= (Button) findViewById(R.id.button11);
        bt12= (Button) findViewById(R.id.button12);
        bt13= (Button) findViewById(R.id.button13);
        bt14= (Button) findViewById(R.id.button14);
        bt15= (Button) findViewById(R.id.button15);
        bt16= (Button) findViewById(R.id.button16);
        bt18= (Button) findViewById(R.id.button18);
        bt19= (Button) findViewById(R.id.button19);
        text= (EditText) findViewById(R.id.editText);
        bt1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=1;
                string2+=1;
                text.setText(string);
            }
        });
        bt2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=2;
                string2+=2;
                text.setText(string);
            }
        });
        bt12.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2==""){
                    string+="0.";
                    string2+="0.";
                }else{
                    string+=".";
                    string2+=".";
                }
                text.setText(string);
            }
        });
        bt16.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!=""){
                id=1;
                string+="+";
                a=Float.valueOf(string2);
                string2="";
                text.setText(string);
                }else
                    text.setText("");
            }
        });
        bt11.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!="") {
                    b = Float.valueOf(string2);
                    if (id == 1) {
                        string = String.valueOf(a + b);
                    } else if (id == 2) {
                        string = String.valueOf(a - b);
                    } else if (id == 3) {
                        string = String.valueOf(a / b);
                    } else if (id == 4) {
                        string = String.valueOf(a * b);
                    }
                    text.setText(string);
                    string2 = "";
                    string = "";
                }else
                    text.setText("");
            }

        });
        bt3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=3;
                string2+=3;
                text.setText(string);
            }
        });
        bt4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=4;
                string2+=4;
                text.setText(string);
            }
        });
        bt5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=5;
                string2+=5;
                text.setText(string);
            }
        });
        bt6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=6;
                string2+=6;
                text.setText(string);
            }
        });
        bt7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=7;
                string2+=7;
                text.setText(string);
            }
        });
        bt8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=8;
                string2+=8;
                text.setText(string);
            }
        });
        bt9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=9;
                string2+=9;
                text.setText(string);
            }
        });
        bt10.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                string+=0;
                string2+=0;
                text.setText(string);
            }
        });
        bt13.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
              if(string2!=""){
                  id=2;
                  string+="—";
                  a=Float.valueOf(string2);
                  string2="";
                  text.setText(string);
              }else
                  text.setText("");
            }
        });
        bt14.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!=""){
                    id=3;
                    string+="%";
                    a=Float.valueOf(string2);
                    string2="";
                    text.setText(string);
                }else
                    text.setText("");
            }
        });
        bt15.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!=""){
                    id=4;
                    string+="X";
                    a=Float.valueOf(string2);
                    string2="";
                    text.setText(string);
                }else
                    text.setText("");
            }
        });
        bt18.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!=""){
                    int a=Integer.valueOf(string2);
                    string2=Integer.toBinaryString(a).toString();
                    text.setText(string2);
                }else{
                    text.setText("");
                }
                string2 = "";
                string = "";
            }
        });
        bt19.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(string2!=""){
                    int a=Integer.valueOf(string2);
                    string2=Integer.toHexString(a).toString();
                    text.setText(string2);
                }else{
                    text.setText("");
                }
                string2 = "";
                string = "";
            }
        });
    }
    
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="com.example.administrator.calculator.MainActivity">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText"
        android:layout_alignParentTop="true"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true"
        android:layout_toEndOf="@+id/textView"
        android:layout_toRightOf="@+id/textView"
        android:clickable="false"
        android:contextClickable="false"
        android:editable="false" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Calculate:"
        android:id="@+id/textView"
        android:layout_alignTop="@+id/editText"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true"
        android:layout_alignBottom="@+id/editText"
        android:textSize="@dimen/abc_text_size_headline_material"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="1"
        android:id="@+id/button"
        android:layout_alignTop="@+id/button2"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="2"
        android:id="@+id/button2"
        android:layout_above="@+id/button16"
        android:layout_alignLeft="@+id/button16"
        android:layout_alignStart="@+id/button16" />

    <Button
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="3"
        android:id="@+id/button3"
        android:layout_alignTop="@+id/button2"
        android:layout_alignLeft="@+id/button6"
        android:layout_alignStart="@+id/button6"
        android:layout_alignRight="@+id/button6"
        android:layout_alignEnd="@+id/button6" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="4"
        android:id="@+id/button4"
        android:layout_above="@+id/button"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="5"
        android:id="@+id/button5"
        android:layout_above="@+id/button2"
        android:layout_alignLeft="@+id/button2"
        android:layout_alignStart="@+id/button2" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="6"
        android:id="@+id/button6"
        android:layout_alignTop="@+id/button5"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="7"
        android:id="@+id/button7"
        android:layout_centerVertical="true"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="8"
        android:id="@+id/button8"
        android:layout_alignTop="@+id/button7"
        android:layout_alignLeft="@+id/button5"
        android:layout_alignStart="@+id/button5" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="9"
        android:id="@+id/button9"
        android:layout_alignTop="@+id/button8"
        android:layout_alignLeft="@+id/button6"
        android:layout_alignStart="@+id/button6" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="0"
        android:id="@+id/button10"
        android:layout_above="@+id/button11"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="="
        android:id="@+id/button11"
        android:textStyle="bold"
        android:textSize="@dimen/abc_action_bar_stacked_max_height"
        android:layout_alignParentBottom="true"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="."
        android:id="@+id/button12"
        android:layout_above="@+id/button11"
        android:layout_alignRight="@+id/button11"
        android:layout_alignEnd="@+id/button11" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="—"
        android:id="@+id/button13"
        android:layout_above="@+id/button7"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="/"
        android:id="@+id/button14"
        android:layout_below="@+id/button18"
        android:layout_alignLeft="@+id/button8"
        android:layout_alignStart="@+id/button8" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="X"
        android:id="@+id/button15"
        android:layout_above="@+id/button9"
        android:layout_alignLeft="@+id/button9"
        android:layout_alignStart="@+id/button9" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="+"
        android:id="@+id/button16"
        android:layout_above="@+id/button11"
        android:layout_centerHorizontal="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Binary"
        android:id="@+id/button18"
        android:layout_above="@+id/button13"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true"
        android:layout_toStartOf="@+id/editText"
        android:layout_alignRight="@+id/button13"
        android:layout_alignEnd="@+id/button13" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="HEX"
        android:id="@+id/button19"
        android:layout_above="@+id/button14"
        android:layout_alignRight="@+id/button15"
        android:layout_alignEnd="@+id/button15"
        android:layout_alignLeft="@+id/button15"
        android:layout_alignStart="@+id/button15" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="DEL"
        android:id="@+id/button17"
        android:layout_alignBottom="@+id/button19"
        android:layout_alignLeft="@+id/button14"
        android:layout_alignStart="@+id/button14"
        android:layout_alignRight="@+id/button14"
        android:layout_alignEnd="@+id/button14" />

</RelativeLayout>
