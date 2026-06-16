## যে যত বড় Developer সে তত বড় Problem Solver ।

activity_main.xml
MainActivity.java
RelativeLayout
LinearLayout

build.gradle.kts (Project: App_Name)
build.gradle.kts (Module :app)
proguard-rules.pro (ProGuard Rules for "app")
gradle.properties (Project Properties)
gradle-wrapper.properties (Gradle Version)
libs.versions.toml (Version Catalog)
local.properties (SDK Location)
settings.gradle.kts (Project Settings)


## 201
Java Basic
ডাটা টাইপ: ডাটার ধরন বা প্রকৃতি।
বিভিন্ন ধরনের তথ্যকেই আমরা ডাটা বলি। আর এই ডাটার প্রকৃতি বা ধরনকেই বলা হয় ডাটা টাইপ।
ভ্যারিয়েবল: ডাটা রাখার জন্য একটি কন্টেইনার।
ভ্যারিয়েবল হলো এক ধরনের কন্টেইনার, যেখানে আমরা ডাটা রাখি। আমরা ভ্যারিয়েবলের মাধ্যমে ডাটা স্টোর করে রাখি।
উদাহরণ:
আপনি একটা বাক্সে (ভ্যারিয়েবল) আপেল (int ধরনের ডাটা) রাখতে পারেন, আবার পরে সেখানে আপনার নাম (string ধরনের ডাটা) রাখতে পারেন। কিন্তু একই সাথে আপেল এবং আপনার নাম দুটোই রাখতে পারবেন না।
## 202
Mainactivity এর মধ্যে java basic code লিখবো ।
Data type Variable;
int  mynumber;
String myname;
int  number1,number2,number3;
int number1=20;
String myname=”Bangladesh”;
লালগুলো হচ্ছে  Data type(Example: int,String ,float,double)  আর নীলগুলো variable । যেখানে just variable নাম (Example: mynumber, number1, number2, number3) দেওয়া আছে সেই কন্টেইনার ভিতরে ফাঁকা মানে Null । আর যেখানে Equal=”ভিতরে লেখা” আছে(Example:number1=20; myname=”Bangladesh”;) অর্থাৎ কন্টেইনারএর ভিতরে(20,Bangladesh) আছে ।
Data type Variable=”data”;
Data type Variable=data;
Variable=”data”;

String mystring = “Hello ” + “World”
String a1=”Hello ”
String a2=”World”


int  num1=10;
int num2=20;
int sum=num1+num2;
int sum=10+20;


Android studio তে এবার চেষ্টা করি ।
Xml file LinearLayout এ নেই ।
LinearLayout এর ভিতরে একটা Textview/Button নেই ।
Mainactivity মধ্যে public class এর নিচে data type(Textview/button) variable(Android:id)
 লিখবো public class এর নিচে, ধরি,
Textview নামে variable নিলাম সাথে xml code textview id টা নিলাম ।
Android:id = Findviewbyid(R.id.Android:id);
Android:id.setText(int float এর যে data থাকে সেগুলো বসাবো)
Android:id.setText(“যা show করাতে চাও” +variable+ (যে variable এ result set করা সেটা । আর আবার + মানে পরবর্তী variable সাথে আনা ।
Example:


## 203
User কিছু Input  দিবে
Linear Layout নিলাম
android:orientation="vertical"
Activity main xml এ <EditText  /> নিলাম
android:id="@+id/edname"একটা id বানিয়ে রাখলাম । 
android:layout_margin="50dp" চারপাশে 50dp জায়গা ছেড়ে দিয়ে মাঝের দিকে কাজ করবে।
android:ems="16" //এটা প্রস্থ বাড়ানোর ক্ষেএ্রে ব্যবহার হয় ।
android:hint="Type your Name" //Hint ব্যবহার করে কোনো Text box এর Input এর Background এ হালকা লেখা দেখা যায় ।
android:inputType="textPersonName"  // User থেকে input নেওয়ার ধরন select করবো   ।
MainActivity Java তে যাই । 
@Override এর উপরে পরিচয় করিয়ে দিবো : 
EditText কে edName ধারা (Example : EditText edName;) 
setContentView এর নিচে পরিচয় করিয়ে দিবো 
edName =findViewById(R.id.edname);

 mybutton.setOnClickListener(new View.OnClickListener() {  //new এরপর gap দিয়ে enter চাপো ।
            @Override
            public void onClick(View v) {
                String username = edName.getText().toString(); // username নামে একটা variable ধরলাম ।  edName এর text নিলাম getText ধারা এবং setText ধার জিনিসটা show করলাম tvdisplay নামক xml android id  তে ।
                tvdisplay.setText("Hello"+username+"Thanks "); //+variable মানে ওর ভিতরে যা আছে তা দেখাবে ।
            }
        });
tvdisplay.setText("Hello"+username+"Thanks "); //setText দিয়ে output কি লিখা থাকবে সেটা নির্দেশ করে ।

Shortcut:: tvdisplay.setText("Hello"+edName.getText().toString()+"Thanks ");



Example: (XML)

android:orientation="vertical"
    android:layout_margin="50dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Email or Number"
        android:textSize="30sp"
        android:textStyle="bold"
        />

    <EditText
        android:id="@+id/edname"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="20"
        android:hint="email@gmail.com or 01********"
        android:inputType="textPersonName"
        android:padding="10dp"
        />

    <Button
        android:id="@+id/button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Log In"
        />
    <TextView
        android:id="@+id/tvdisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text=""

        />

</LinearLayout>


Example(Java)::
package com.timeforschool.tfs;
import….;
public class MainActivity extends AppCompatActivity {
    EditText edName;
    Button mybutton;
    TextView tvdisplay;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

        edName=findViewById(R.id.edname);
        mybutton=findViewById(R.id.button);
        tvdisplay=findViewById(R.id.tvdisplay);

        mybutton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String username = edName.getText().toString();
                tvdisplay.setText("Hello"+username+"Thanks ");
            }
        });

        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }
}


## 204

যে মান নেই না কেন সবগুলোই স্ট্রিং হয়ে যায় পরে সেগুলোকে কনভার্ট করতে হয়।
সংখ্যা ব্যবহার করতে চাইলে xml এ ইনপুট টাইপ নাম্বার ডেসিমেল ইউজ করব।

EditText variable;
variable=findViewById(R.id.xml android id);
Convert : setOnClickListener এর ভিতরে
String variable = edName.getText().toString();

একটা সংখ্যা user দিবে সেটা string হিসেবে দিলেও সেটাকে Integer এ  convert করবো ।
int byprice;
String vaimy = edName.getText().toString();
byprice=Integer.parseInt(varimy);
Shortcut::
int byprice=Integer.parseInt(edName.getText().toString());




## 205
যদি অ্যান্ড্রয়েড স্টুডিওতে অনেকগুলো Red Bug দেখা যায় তাহলে আমাদের sync now করতে হবে। তারপর File এ Click দিবো invalidate caches/Restart এ Click দিবো Invalidate & Restart ।
আরো করতে পারি Build থেকে Clean Project এ click করবো । এতে করে এতে করে পুরাতন ফাইলগুলোর অবশিষ্ট অংশ চলে যাবে।
Build থেকে rebuild  এ Click দিবো । তাহলে program আবার build হবে ।
যদি Java তে কোনো ভুল করি তাহলে Apps - × Close app / Stop / App open হয়ে সাথে সাথে close হয়ে যাবে। App crash করলো। App crash error solve এর জন‍্য বামে নিচে Logcat Option এ Click করবো। তারপর Verbose option থেকে error option select করে error গুলো দেখতে পাবো। আরো ডানে Show only selected application এ click করে রাখবো। যে স্থানে Java পরিচয় করিয়ে দেওয়া অথবা অন‍্য কিছু একটা miss করছি code এ ঐ স্থানে click করলে app crash করবে। Stackoverflow তে সবধরনের সমাধান পাবে। Edit এ টিপ দিয়ে Undo Redo option পাবো।
আর যদি XML এ Error হয় তাহলে Android studio থেকেই Red Error দেখাবে আর App installation পর্যন্ত যাবে না।Build output a error দেখাবে।
নতুন Project open করার জন‍্য :: File থেকে শুরুতে 5 নম্বরে দেখো close project লিখা আছে ঐখানে চাপো তাইলে আগের project ঐ অবস্থায় বন্ধ হয়ে new project শুরু করার option আসবে।
New project থেকে Empty Activitiy তে চলে যাবো 


206
207
Github  এ code uploaded BMI
208
209
Operations
&& দুইটার দুইটাই সত্য হলে কাজ করবে । এমন অনেকগুলোও হতে পারে । 
 ||  দুইটার একটা সত্য হলেই কোড কাজ করবে ।
! 
 < 
> 
+
-
%
*
/

210
Even odd find
211
If else basic format
212
If else basic format apply in bmi
213
Show error on input file / null click error
User যদি কোনো ডাটা  না দেয় । আর Result Button এ click দেয় তাহলে app crash করবে । এটি এড়ানোর জন্য সম্পূর্ন লজিককে অথবা java code এর setOnClickListener এর ভিতরের code কে if else condition এ আনতে হবে । কিছুটা এমন যে : যদি  user যা দিবে তার length 0 থেকে বেশি হয় তাহলে ভিতরের লজিক কাজ করবে ।
if(useridbox1.length() >0 && useridbox2.length() >0 && useridbox3.length() >0 ){
…..Logic……
}
else{
Toast.makeText(MainActivity.this, "Please Enter a Number", Toast.LENGTH_LONG).show();
}
অথবা warning ও দিতে পারি : 
else{
edweight.setError("Please Enter a Number");
}
214,215,216,217 github acode
218 করতে হবে ।
219 
## Text to Voice
@Override
protected void onCreate(Bundle savedInstanceState) {
   super.onCreate(savedInstanceState);
   EdgeToEdge.enable(this);
   setContentView(R.layout.activity_main);
//On create bundle এর মাঝে পরিচয় করিয়ে দেই input এবং বাটন এবং একটা নতুন variable textToSpeech ধরি। 
   EditText edtexts=findViewById(R.id.edtext); //inputএর জন‍্য 
   Button edbutton=findViewById(R.id.button);//বাটন টিপ দেওয়ার জন‍্য 
   TextToSpeech textToSpeech;
//নতুন variable ধরি। এটা এভাবেই লাগবে যদি কথা শুনতে চাও।
   textToSpeech=new TextToSpeech(MainActivity.this, new TextToSpeech.OnInitListener() {
//textToSpeech এর পর সমান চিহ্ন দেও এরপর TextToSpeech ধরে যেই Activity মধ‍্যে শব্দ শুনাবো  সেখানে রাখবো। 
       @Override
       public void onInit(int status) {

       }
   });

//button এর setOnClick listener ধরবো।
   edbutton.setOnClickListener(new View.OnClickListener() {
       @Override
       public void onClick(View v) {

           if(edtexts.length()>0){
           //শব্দ শুনতে চাইলে variable টাকে ধরে ডট দিবো speakএর মাঝে user data অথবা সেট করা ডাটা নিয়ে ডট দিবো তারপর TextToSpeech ধরবো ডট দিবো Queue flush মানে এই মুহুর্তে শব্দটা পড়ো।আর utteranceld মানে উচ্চারণ এটা null দিলে system এর default voice নিবে auto 
textToSpeech.speak(""+edtexts.getText().toString(), TextToSpeech.QUEUE_FLUSH, null, null);
       }else{
               textToSpeech.speak("Please write something.", TextToSpeech.QUEUE_FLUSH, null, null);
               edtexts.setError("Please, write something.");}
       }     });

## 220
Alert 
App এর Screen এর মাঝে দেখায় যে  Do you want to exit? Yes No click করলে app থেকে বের করে দেয়(yes) অথবা যেখানে আছে সেখানেই থাকে ।
Apps এর কোনো একটা বাটন চাপলে সেইটা show করবে এখন
On create bundle এর ভিতরে প্রথমে xml বাটন id পরিচয় করাই  findviewbyid দ্বারা
বাটন থেকে একটা setonclicklistener ধরবো ।
new AlertDialog.Builder(MainActivity.this)
.setTitle("This is a title") // মাঝে show হওয়া বড় লেখাটা Do you want to exit?
.setMessage("Message") // মাঝে show হওয়া বড় লেখাটা নিচে অনেকসময় ব্যবহার করে খুবই কম।
.setCancelable(true) //এটা দিলে user ঐ বক্স বাদে অন্য কোথাও টাচ করলে বক্সটা চলে যাবে।
.setCancelable(false) //এটা দিলে user ঐ বক্স বাদে অন্য কোথাও টাচ করলে কাজ করবে না বক্স এর বাটনই চাপতেই হবে ।।(userfriendly)

User এর জন্য option (Yes No Agree Disagree)এই বাটনগুলো কিভাবে তৈরি করবো । 

এতক্ষন যা করলাম তা করার পর 
.setNegativeButton("Cancel", new DialogInterface.OnClickListener() {
//ডটSetnegativebutton দেওয়ার পর “” ভিতরে যা বসাবো তা হলো Option এ show করবে Yes No Cancel.. কমার পর new লিখে গেপ দিলে Dialoginferface আসে তা selected করবো। 
   @Override
   public void onClick(DialogInterface dialog, int which) {
       buttons.setText("Hi");
// যেই বাটনে চাপার পর Yes No option আসছিলো ঐ  বাটনের আগের text পরিবর্তন হয়ে Hi ঊঠবে এখন। 
Toast.makeText(MainActivity.this, "Its just a toast. You can also use in here", Toast.LENGTH_LONG).show();

   }
})
ইউজার থেকে পজিটিভ রেজাল্ট(yes) চাইলে আমরা পজিটিভ ইউজ করি আর নেগেটিভ(cancel) রেজাল্ট চাইলে আমরা নেগেটিভ ইউজ করি আর ধরো এরকম যেগুলা নিউট্রাল আছে এগুলো আমরা নিউট্রাল ইউজ করি।


## 221
User back বাটনে click করলে Do you want to exit ? yes no select করবে

onCreate(Bundle এর দ্বিতীয় বন্ধনীর থেকে বাহিরে  গিয়ে mouse এর Right click করবো Generate লিখায় চাপ দিবো এরপর Overright Method এ যাবো । তারপর onBackPressed সার্চ দেও । select করে enter করো //super.onBackPressed();
এটাকে comment বানাই দেও কারণ এটা থাকলে back button চাপলে app close হয় but পরে ঢুকলে ঐyes no exit notification আবার দেখায় । 
new লিখার পর   AlertDialog.Builder(MainActivity.this) সেট করবো ।
ঐ মেসেজের পাশে ছবি লাগাতে চাইলে Drawable এ ছবি paste করবো । তারপর 
.setIcon(R.drawable.imagename)
finishAndRemoveTask();//এটা দিলে ঐখানে চাপলে সরাসরি app থেকে বের করে দেয় ।// lollipop এর নিচের vertion এ  finishAndRemoveTask কাজ করবে না ।
dialog.dismiss(); // এ চাপলে user no/cancel এ চাপলে ঐ কাজটা off হয়ে যায় ।

## 222
Internet check
Manifest এ লিখবে 
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>


একটা বাটন নেও এবং free textview নেও ।
onCreate(Bundle এর ভিতর 
Java তে Button buttons=findViewById(R.id.button); লিখলাম ।
Button.setonclicklistener নিলাম তার ভিতরে 
 
ConnectivityManager connectivityManager= (ConnectivityManager) getSystemService(Context.CONNECTIVITY_SERVICE);

 NetworkInfo networkInfo=connectivityManager.getActiveNetworkInfo();

If else statement দিয়ে তার ভিতরে AlertDialog নিয়ে মেসেজ show করবো ।
## 223
Offline Music Play App 
XML Button create করা
Java তে পরিচয় করিয়ে দেওয়া ।
Offline একটা music copy করে res folder   এর উপর mouse রেখে mouse right click করলে New তরপর Directory চাপলাম then একটা নাম দিলাম raw এবং enter চাপলাম । এবার raw এর উপর paste করলাম audio টা। 

Music run করতে গেলে  MediaPlayer java class এর help নিতে হবে । Than mediaPlayer variable ধরলাম
MediaPlayer mediaPlayer;
এবার onCreate Bundle এর ভিতরে mediaPlayer যে variable টা ধরলাম সেটা Assign করতে হবে। তাই button.setonclickListener ধরলাম new দিয়ে নিলাম। এরপর mediaPlayer=MediaPlayer.create(MainActivity.this,R.raw.offlinemusicidname);
এরপর mediaPlayer.start(); করে দিবো  
MediaPlayer.create তখনই ব্যবহার করবো যখন audio file offline drawable থেকে access করবো ।

## 223

Online Music Play App 
বাটন থেকে Setonclicklistener নিলাম। 
তারপর mediaPlayer variable এর মাঝে নতুন করে new MediaPlayer পরিচয় করিয়ে দিলাম।
এরপর mediaPlayer.setDataSource(“Link বসাবো ”); error থেকে Surround with try/catch নিবো। 
তারপর mediaPlayer.setDataSource এর নিচে 
mediaPlayer.prepare();//ইন্টারনেট নিয়ে প্রস্তুত হচ্ছে।
mediaPlayer.start();
নেওয়া।
try/catch এর কাজ হলো। যখন ইন্টারনেট এবং লিঙ্ক থেকে একটা audio play করার চেষ্টা করছেন। তখন অনেক ধরনের সমস্যা আসতে পারে।যেমন : user এর ফোনে নেট নাই but user চেষ্টা করছে audio চালানোর তখন app crash করবে। 
তো এখানে কোনো error আসলে program প্রথমে try করে এবং সেটা না হলে catch এ গিয়ে e.printStackTrack(); দিয়ে সামলাই নেয়। 

onClickListener এর মধ‍্যে এই লাইনটা লিখবো : if (mediaPlayer != null)mediaPlayer.release();
এর মানে হচ্ছে:

এটি নিশ্চিত করে যে, মিডিয়া প্লেয়ার ব্যবহারের পর সঠিকভাবে তা বন্ধ করা হয়েছে এবং কোনো মেমরি লিক (memory leak) হবে না।
গানটি বন্ধ করার জন্য আপনাকে release() ব্যবহার করতে হবে।

আপনি ত সবসময় আপনার app এর মন মত song/Tone পাবেন না তাই আপনি চাইলে যেকোনো একটা server ব‍্যবহার করে তাদের ঐখানে upload করে mp3 link create করে কাজটি করতে পারেন। আর সব website এ song এর link এর শেষে.mp3  থাকে না। তাই নিজের website এ সেটা বানাই নিতে হয়।

## 224
Basic Music Play App try 

কোনো java variable এর নাম public static এর ভিতরে রাখলে এটাকে যেকোনো java class থেকে Access করা যাবে ।

## 225
Basic PDF App 

Search : android pdf viewer library github barteksc
https://github.com/barteksc/AndroidPdfViewer
https://github.com/DImuthuUpe/AndroidPdfViewer

কিভাবে AndroidPdfViewer Library Implement করবেন ? নিচে দেওয়া step গুলো follow করুন । ✅
--------------------
১। PDF Library
build.gradle.kts (Module :app) এ কোডঃ
implementation 'com.github.DImuthuUpe:AndroidPdfViewer:3.1.0-beta.1'
implementation ("com.github.barteksc:android-pdf-viewer:3.2.0-beta.1")
২। settings.gradle > inside the repositories
কোডঃ
maven { url 'https://jitpack.io' }
৩। gradle.properties (Project Properties) শেষে লিখবো কোডঃ
android.enableJetifier=true





৪ । proguard-rules.pro (ProGuard Rules for "app") এ
-keep class com.shockwave.**

ProGuard কি? 
Proguard হলো app এর security system। যেটার মাধ‍্যমে app কে কেউ Reverse engineering করে তাহলে কিভাবে কোড ভেঙ্গে যেতে পারে সেগুলোর নিশ্চিত করা হয়।

৫ । Activity_main.xml  এ RelativeLayout নিবো তার ভিতরে textview কেটে বসাবো ::

<com.github.barteksc.pdfviewer.PDFView
        android:id="@+id/pdfView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>


Error version ( OpenJDK 64-Bit Server VM by JetBrains s.r.o.) : এখন যদি com.github.barteksc.pdfviewer.PDFView এর মধ্যে red error আসে তাহলে 

maven { url("https://jcenter.bintray.com") }

Error Another version : 
build.gradle.kts (Project: App_Name) এর allprojects ভিতর 

allprojects {
    repositories {
        google()
        mavenCentral()
        maven { url "https://jitpack.io" }
        maven { url "https://jcenter.bintray.com" }
    }
}



এরপর github link এর নিচের দিকে Load a PDF file OPTION এ যাবো সেখান থেকে আমার কাজের প্রয়োজন অনুসারে যেকোন টি ব‍্যবহার করতে পারি।এখন Load নিয়ে কাজ করবো। 


PDFView pdfView=findViewById(R.id.pdfView);


pdfView.fromAsset("")
               .load();

Asset folder create করতে হবে ।

App>> Mouse Right button >> New >> Folder >> Assets Folder >> main >> Finish

PDF file টি paste করবো । NAME SMALL LETTER এর হতে হবে ।






PDFView pdfView=findViewById(R.id.pdfView);


## 225
Shared Preferences   
User app close করলেও data save থাকবে phone storage এ। 
দুইটা Activity দিয়েও কাজটি করতে পারি।




activity_main.xml
MainActivity.java
AndroidManifest.xml
RelativeLayout
LinearLayout

build.gradle.kts (Project: App_Name)
build.gradle.kts (Module :app)
proguard-rules.pro (ProGuard Rules for "app")
gradle.properties (Project Properties)
gradle-wrapper.properties (Gradle Version)
libs.versions.toml (Version Catalog)
local.properties (SDK Location)
settings.gradle.kts (Project Settings)


## 237:

Layoutinflater মানে একটা XML Activity মধ‍্যে আরেকটা XML Activity রাখবো। ঐ page টা আলাদা একটা XML এ Create করে than এই Code দিলেই চলে আসবে। 

<include
layout="@layout/activity_name_enter_here"
/>


একটা জিনিস মনে রাখতে হবে কখনোই এই দুইটা XML এর মধ‍্যে যে জিনিসগুলো ব‍্যবহার করবো একটা জিনিসের id র আসে যাতে আরেকটা না মিলে। একই ছবি দুইটা Activity মধ‍্যে ব‍্যবহার করে একই id দিয়ে ডাকলে App ক্রাস করার সম্ভাবনা থাকে। Playstore এ reject খাবে।
এই যে একটি XML Activity মধ‍্যে আরেকটা বরলাম এখন ঐ XML এর File গুলোও Java তে সহজে find view id দিয়ে খুজে বের করতে পারবো।

238:

Inflate layout::

layoutInflater = getSystemService(Context.LAYOUT_INFLATER_SERVICE);
Click :  Cast expression to “”
Int resource = যে লেআউট টা কে ঢুকাতে চাই  তার আইডি
ViewGroup root = এই লেআউট এ দেখতে চাই  তার আইডি
1-10 min পর্যন্ত কোড গুলোর মধ্যে সুন্দরভাবে ব্যাখ্যাগুলো বাংলাতে লেখা আছে গিট হাবে  Activity main java file 1

11-20 min পর্যন্ত একটা Layout এর কোনো কিছুতে click করলে আরেকটা Layout inflate হয়। এখন এই inflate layout এর কোনো কিছুতে click করলে সেটা কাজ করা শিখবো।সেখানে toast দিবো এবং বাকী সব কিছু করতে পারবো । Activity Main Java 2  https://github.com/arshahrear30/layoutInflater/blob/main/Activity%20Main%20Java%202

238:
Xml ListView এর সুবিধা
সহজ ডেটা প্রদর্শন: ডেটার লম্বা তালিকা খুব সহজে এবং ব্যবহারকারী-বান্ধব উপায়ে দেখানো যায়। অনেক আইটেম তার পেটের মধ্যে ধারন করতে পারে । প্রত্যেকটা আইটেম দেখতে কেমন হবে সেটা আলাদা একটা xml এ ডিজাইন করি ।
Scroll Functionality: ডিফল্টভাবে ScrollView-এর মতো স্ক্রোল করার সুবিধা দেয়।
ইভেন্ট হ্যান্ডলিং: ListView-তে আইটেম সিলেক্ট করার জন্য onItemClickListener ব্যবহার করা যায়।
ডাইনামিক ডেটা আপডেট: Adapter ব্যবহার করে ডেটা ডাইনামিকভাবে আপডেট করা যায়।
কাস্টম লেআউট: ListView-তে প্রতিটি আইটেমের জন্য কাস্টম লেআউট ব্যবহার করা যায়।
কম RAM ব্যবহার: RecyclerView-এর আগে এটি কম RAM ব্যবহার করে এবং ছোট ডেটাসেটের জন্য যথেষ্ট কার্যকরী।
Simple Adapter Integration: বিভিন্ন ধরনের অ্যাডাপ্টার যেমন ArrayAdapter, SimpleCursorAdapter, অথবা কাস্টম অ্যাডাপ্টারের মাধ্যমে ডেটা লোড করা যায়।
অফলাইনে বা অনলাইনে ডেটা লোড করার জন্য উপযোগী।
ListView মূলত ছোট ডেটাসেটের জন্য দ্রুত ডেটা প্রদর্শনের আদর্শ উপায়। যাইহোক, বড় ডেটাসেটের জন্য RecyclerView বেশি কার্যকর।

239:
Listview এর প্রাথমিক xml (Activity_main.Xml) এর ভিতর 

<ListView
        android:id="@+id/listview"
        android:layout_width="match_parent"
        android:layout_height="100dp"
/>
এটা auto scrollview সুবিধা দেয় । এর ভিতরে ডিজাইন করার জন্য আরেকটা xml file নিতে হবে ।(xml এর উপর mouse রেখে mouse right button click -> New -> XML -> Layout xml File ->Layout file name  -> নাম দরলাম -> item

Drawable এ ছবি এনে phaste করবো ।

এখন দুইটা xml কে এক করার জন্য layoutinflater use করতে হবে। আর layoutinflater কে globally declare করবো(Best practice)।এটার জন্য adapter টার ভিতরে উপরে বসালেই globally কাজ করবে।

240
HashMap হল দ্রুত সার্চ, অ্যাড, ডিলিট সুবিধা দেয়।অ্যান্ড্রয়েড অ্যাপে Data Structure বা Config ম্যানেজমেন্টে খুবই কাজের।
HashMap এর গুরুত্বপূর্ণ ফিচার:
Key Unique হয় → একই Key দ্বিতীয়বার দিলে পুরনো Value রিপ্লেস হয়ে যায়।
Null Key ও Null Value রাখতে পারে।
Fast Access → Key দিয়ে দ্রুত Value খুঁজে পাওয়া যায়।
Order Maintain করে না। (যেমন: LinkedHashMap করলে order থাকে)


HashMap হল একটা ক্লাস, যেটা java.util প্যাকেজে আছে। এটা এমন একটা জায়গা যেখানে আপনি একটা Key এবং তার সাথে একটি Value স্টোর করেন। পরে ঐ Key ব্যবহার করে Value বের করতে পারেন।
ধরুন, আপনি একটা টেলিফোন ডাইরেক্টরি বানাতে চান, যেখানে Name = Key এবং Phone Number = Value হবে।

HashMap   এ  যেটাকে key বলা হয় সেটা আসলে Table Name

 ListView mylistview;
 ArrayList arrayList=new ArrayList<>();
 এইটুকু লেখার ফলে একটা ফাঁকা টেবিল তৈরি হল ।

## 244
ScrollView একা কাজ করতে পারে না সেজন্য এর ভিতরে লিনিয়ার লেআউট অথবা রিলেটিভ লেআউট দিয়ে কাজ করতে হয় ।

Use this website for icon : https://icons8.com/  (icon এ website logo থাকে )

 public static ভেরিয়েবল ধরলে যে কোন java class থেকে access করা যাবে |
android:foreground="?attr/scrimAnimationDuration"   
GridView :  পাশাপাশি কলাম করতে চাইলে GridView  ইউজ করি ।
