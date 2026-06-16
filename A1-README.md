
Windows+V=History of clipboard
Windows+D=Hide all screen

Download Android Studio.যখন install করবে must internet connection লাগবে 6-7 ঘন্টা। Text write .Image Add.
Docs a Code paste করলে background black remove করার জন্য 
Click : Format 
Last option : Clear Format

##Neomorphism style setup##

settings.gradle (Project Settings)::
mavenCentral()
gradlePluginPortal()
maven {url "https://jitpack.io"}
google()
mavenCentral()
maven {url "https://jitpack.io"}


build.gradle (Module :app) ::
implementation 'com.github.fornewid:neumorphism:0.3.2'
or,
implementation("com.github.fornewid:neumorphism:0.3.2")



Not important 
Remember to add MultiDex on app gradle:
implementation("androidx.multidex:multidex:2.0.1")
multiDexEnabled true
AND minSdkVersion 21

More Details about Neumorphism - (GitHub): https://github.com/fornewid/neumorphism
https://github.com/4inodev/Neomorphic-FrameLayout-Android
implementation("com.github.fornewid:neumorphism:0.3.2")
jcenter() 
maven { url = uri(  "https://jitpack.io" )}

##Page Connection:##

Button Class6;
Class6=findViewById(R.id.class6);
Class6.setOnClickListener(new View.OnClickListener() {	
           @Override
	public void onClick(View v) {
    	Intent Class6= new Intent(MainActivity.this, MainActivity2.class);
    	startActivity(Class6);
	}
});


NeumorphCardView startbutton=findViewById(R.id.start);
startbutton.setOnClickListener(new View.OnClickListener() {
   @Override
   public void onClick(View v) {
       Intent startbutton=new Intent(MainActivity.this,MainActivity2.class);
       startActivity(startbutton);
   }
});





বাটন টাইপ একটা নতুন নাম দিব=fiলিখলে findViewById()আসবে । তারপর () মাঝে R.id লিখবো আবার ডট দিবো তারপর id যেটা set করছিলাম xml file এ ঐটা লিখবো ।  
নতুন নাম ডট setOnClickListener( এবার new টাইফ করে blank দিলে recomendation আসবে। View.OnClickListener এ  চাপ দিবো ।
Intent লিখবো তারপর নতুন নাম =N লিখলে recomendation আসবে ।new Intent()চাপ দিবো । click button যে activity তে আছে তার নাম ডট this কমা, নতুন activity page name ডট class । এরপর; সেমিকোলন দিয়ে নিচের লাইনে startActivity(নতুন নাম)সেমিকোলন

##findViewById  এর shortcut ব্যবহার##
@Override এর উপরে variable ধরে  onCreate(Bundle এর ভিতরে variable=findViewById(R.id.xmlidname);  Example :: 
Button variable;
  @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

        variable=findViewById(R.id.xmlidname);

##Shortcut ::## 
@Override
protected void onCreate(Bundle savedInstanceState) {
   super.onCreate(savedInstanceState);
   EdgeToEdge.enable(this);
   setContentView(R.layout.activity_main);
    Button variable=findViewById(R.id.xmlidname);

পার্থক্য দেখো :: আগে কিন্তু override এর উপর variable একবার setup করতে হতো তারপর নিচে এসে findviewbyid নিয়ে কাজ করতে হতো । এখন shortcut এ দেখো এ কাজটা এক লাইনে করতে চাইলে override এর নিচে onCreate(Bundle এর নিচে setContentView এর নিচে 
Button variable=findViewById(R.id.xmlidname); এইটা একসঙ্গে লিখতে হবে ।

##Tazbi Button এর backend এ কাজ :## 
TextView tvcountid; 
int count;// count নামে variable ধরলাম
Onclick এর ভিতরে 
count++;//
tvcountid.setText(""+count);


##Toast:##
Toast.makeText(MainActivity.this,"Wright here",Toast.LENGTH_SHORT ).show();
 

##Open New Activity##


Java >> MainActivity>>Mouse Right click>>New>>Activity>>Empty View Activity>>Activity name দিবো



##Web View:##
Xml file a Linear Layout নিয়ে ।<Web view সবগুলো match parent & id নিবো  />
Activity Java তে যাবো 

Webview variablename;
@Override
    public void onBackPressed() {
        if( variablename.canGoBack()) {
            variablename.goBack();
        } else {
            super.onBackPressed();
        }
    }

উপরে ১ লাইন
@Override এর নিচে এই তিন লাইন

variablename=findviewById(R.id.webid);
variablename.setWebViewClient(new WebViewClient());
variablename.getSettings().setJavaScriptEnabled(true);
variablename.loadUrl(“url paste here”);
variablename.getSettings().setDomStorageEnabled(true);
variablename.getSettings().setSupportMultipleWindows(true);
CookieManager.getInstance().setAcceptCookie(true);


AndroidManifest এ যাবো 
    xmlns:tools="http://schemas.android.com/tools">

<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />


    <application
লাল লেখাটা দুই টার মাঝে বসাবো 
Example code:
package com.timeforschool.myapplication;


import android.os.Bundle;
import android.webkit.CookieManager;
import android.webkit.WebChromeClient;
import android.webkit.WebView;
import android.webkit.WebViewClient;


import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;








public class MainActivity extends AppCompatActivity {
   WebView webmView;


   @Override
   public void onBackPressed() {
       if(webmView.canGoBack()) {
           webmView.goBack();
       } else {
           super.onBackPressed();
       }
   }


   @Override
   protected void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);
       EdgeToEdge.enable(this);
       setContentView(R.layout.activity_main);










       webmView=findViewById(R.id.webmyid);
       webmView.getSettings().setJavaScriptEnabled(true);
       webmView.setWebViewClient(new WebViewClient());
       webmView.loadUrl("https://aparsclassroom.com/shop/");
       webmView.getSettings().setDomStorageEnabled(true);
       webmView.getSettings().setSupportMultipleWindows(true);
       CookieManager.getInstance().setAcceptCookie(true);


       ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
           Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
           v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
           return insets;
       });
   }
}



##Image Collect from Online for light apk:##

build.gradle.kts(Module :app)
implementation ("com.squareup.picasso:picasso:2.8")
Give internet permission
 <uses-permission android:name="android.permission.INTERNET" />
 <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

Id set করা । আমরা offline image এর জন্য android:src="@drawable/locationname"এটা ব্যবহার করি । But online থেকে নেওয়ার জন্য id দিয়ে নেই ।
Java set করবো 
NeumorphImageView variablename;


 variablename = findViewById(R.id.idname);


Picasso.get()
               .load("URL")
                       .into( variablename);

অনেক সময় user internet slow থাকলে user কে ঐ স্থানে কিছু একটা দেখাতে হলে .placeholder(R.drawable.imagename) ব্যবহার করতে পারি ।

.resize(width,height) এর ব্যবহার : Online এর image অনেক ছোট/বড় থাকে তখন সেটাকে resize করতে ব্যবহৃত হয় ।
.error(R.drawable.imagename) অনেক সময় user internet না থাকলে অথবা যেকোনো error হলে কোন image show করবে।

##Lottie File Setup:##
https://lottiefiles.com/blog/working-with-lottie-animations/getting-started-with-lottie-animations-in-android-app

1.implementation ("com.airbnb.android:lottie:6.5.1")
2.<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
3.res এর উপর মাউস Right button click দিয়ে New তারপর Directory তে নাম দিবো raw তারপর Enter।

4.Chrome লিখো free lottie android studio animation download  
link: https://lottiefiles.com/free-animations/android-studio
5.Select >> Click >> Download >> Automatic go in New Tab >> Lottie JSON Click >> File এ গিয়ে Copy করে res এর raw তে paste করবো >>New Name দিবো ok >> নিচের কোডটা লিখবো এবং animationname এর জায়গায় New Name লিখবো ।

5.<com.airbnb.lottie.LottieAnimationView
    android:id="@+id/animationView"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    app:lottie_rawRes="@raw/animationname"
    app:lottie_autoPlay="true"
    app:lottie_loop="true"/>

6.Download ছাড়াই online থেকে নিতে চাইলে
//app:lottie_rawRes="@raw/animationname"
এই লাইনের পরিবর্তে 
//app:lottie_url="Asset link"
এই লাইন বসাবো ।

7.Asset link কিভাবে পাবো ? 
Download & Handoff>>Handoff>>Enable Asset Link>>Enable>>Asset link>>Copy >>code এ Asset link এর স্থানে paste করো ।

8.app:lottie_autoPlay="true"এই লাইনের মানে এটা click ছাড়া auto play হবে ।
False দিলে click করলে কাজ করবে ।
app:lottie_loop="true" মানে বার বার animation হবে । 
False দিলে একবার হয়ে থেমে যাবে ।

Add Type: Banner Ad Mobile apps,Interstitial/Full screen Add Mobile apps,Rewarded Video Add Mobile apps,Native Add Mobile apps, App Selling ,পারচেস Option,Remove logo,Subscription,2 App same concept 1 free add,1 premier  


##Addmob add implement:##

https://developers.google.com/admob
https://developers.google.com/admob/android/quick-start
Configure your app-এটা skip করতে পারি।নতুন version গুলোতে এটা auto set থাকে।
On click listener তখনই কাজ করে যখন user click করে ।
Step 1:Gradle Module app এ library implementation
implementation 'com.google.android.gms:play-services-ads:23.3.0'

Step 2: ENABLE Internet permission:

<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="com.google.android.gms.permission.AD_ID"/>

Android 13 up phone ar jonno ai text add kora must


Step 3 : AndroidManifest এ <application এর মাঝে 
<meta-data
        android:name="com.google.android.gms.ads.APPLICATION_ID"
        android:value="ca-app-pub-3940256099942544~3347511713"/>
Application id পাবো তখন যখন admob এ account খুলে app upload দিবো।যখন আমরা apps তৈরি করবো তখন ভুলেও আমার তৈরি id দিয়ে বার বার app run করা যাবে না। এতে admob ban হয়ে যাবে। Final release  এর সময় id বসাবো। এর আগ পর্যন্ত website এ যেটা sample id আছে ঐটা ব‍সাবো।

Step 4: Main activity set content view এর পরে 

 new Thread(
            () -> {
  // Initialize the Google Mobile Ads SDK on a background thread.
       MobileAds.initialize(this, initializationStatus -> {});
        })
      .start();

//MobileAds এ import class option আসবে না যতক্ষন পর্যন্ত কোনো একটা app code পরিপূর্ন না বসাবে ।
Alt+Enter চেপে import class এ click দিবো।

##Banner Ad##

Step 1:
Java এর MainActivity তে শেষের } - সেকেন্ড ব্রেকেটের আগে লিখবো অথবা
{
@Override
protected void onCreate(Bundle savedInstanceState) {
- - - - - – - -
}
এখানে লিখবো
}


// Step 1 : Implementation Admob banner ads method in your Activity
private void loadBanner(LinearLayout adViewContainer) {

   // Create a new ad view.
   AdView adView = new AdView(this);
   adView.setAdSize(getAdSize(adViewContainer));
   adView.setAdUnitId("ca-app-pub-3940256099942544/9214589741");

   // Replace ad container with new ad view.
   adViewContainer.removeAllViews();
   adViewContainer.addView(adView);

   // Start loading the ad in the background.
   AdRequest adRequest = new AdRequest.Builder().build();
   adView.loadAd(adRequest);
}

private AdSize getAdSize(LinearLayout adViewContainer) {
   // Determine the screen width (less decorations) to use for the ad width.
   Display display = getWindowManager().getDefaultDisplay();
   DisplayMetrics outMetrics = new DisplayMetrics();
   display.getMetrics(outMetrics);

   float density = outMetrics.density;

   float adWidthPixels = adViewContainer.getWidth();

   // If the ad hasn't been laid out, default to the full screen width.
   if (adWidthPixels == 0) {
       adWidthPixels = outMetrics.widthPixels;
   }

   int adWidth = (int) (adWidthPixels / density);
   return AdSize.getCurrentOrientationAnchoredAdaptiveBannerAdSize(this, adWidth);
}

//Red error Solve : Alt+Enter এ চাপ দিবো Import  class এ চাপ দিবো।

Step 2:

XML1✅XML এর যে page এ Banner ad করতে চাই তার main layout এর bracket এর ভিতরে লিখবো


<LinearLayout
   android:id="@+id/adContainerViewid"
   android:layout_width="match_parent"
   android:layout_height="wrap_content"
   android:orientation="vertical"
   />


Or write : XML2❌

<com.google.android.gms.ads.AdView
xmlns:ads=""https://schemas.android.com/apk/res-auto"
android:id="@+id/adContainerViewid"
android:layout_margin="20dp"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:orientation="vertical"
android:layout_alignParentBottom="true"
android:layout_marginBottom="15dp"
android:layout_marginTop="15dp"
</ com.google.android.gms.ads.AdView>

Step 3:
Main activity set content view এর পরে 

 new Thread(
    —--------
      .start();
এই লেখার পর নিচের লিখাটা লিখবো :✅

// Finding adViewContainer and call loadBanner() method
LinearLayout adContainerView= findViewById(R.id.adContainerViewid);
loadBanner(adViewContainer);



Or write:❌
@Override এর উপর লিখো:
LinearLayout adContainerView;

তারপর .start(); এর পর লিখো : 

adContainerView = findViewById(R.id.adContainerViewid);
loadBanner(adViewContainer);


Step  4:
findViewById এর নিচের লাইনে লিখো : 
// Create a new ad view.yt
       AdView adView = new AdView(this);
       adView.setAdUnitId("ca-app-pub-3940256099942544/9214589741");
       adView.setAdSize(AdSize.BANNER);


// Replace ad container with new ad view.yt
       adContainerView.removeAllViews();
       adContainerView.addView(adView);


// Start loading the ad in the background.Zsir
       AdRequest adRequest = new AdRequest.Builder().build();
       adView.loadAd(adRequest);




https://youtu.be/1Buk-j34D5A?si=PzWZTfIOc1moQORR&t=1040
https://learnwithdebasish.blogspot.com/2024/06/admob-ad-implementation-2024-in-java.html

Finally: https://www.youtube.com/watch?v=5OKibZ5GN3k

##Interstitial Ad##
https://youtu.be/yO9yRdOGztk?si=ZcG522ZwFfZ--iyp
Step 1:
Main Activity সবার উপরে 
package com.timeforschool.myapplication;
public class MainActivity extends AppCompatActivity {

এখানে লিখবো: InterstitialAd mInterstitialAd;
{

Step 2:
Java এর MainActivity তে শেষের }  সেকেন্ড ব্রেকেটের আগে লিখবো অথবা
{
@Override
protected void onCreate(Bundle savedInstanceState) {
- - - - - – - -
}
এখানে লিখবো
}

// FullScreen Ads
// Step 2 : loadFullscreenAd
   private void loadFullscreenAd() {
       AdRequest adRequest = new AdRequest.Builder().build();
//একটা page এ ২ বার adRequest দিলে adRequest নামটা adRequest22 অর্থাৎ change করে দিবো ।যদিও এক page এ ১ বারের বেশি adRequest দেওয়ার দরকার নেই । 
       InterstitialAd.load(this, "ca-app-pub-3940256099942544/1033173712", adRequest,
               new InterstitialAdLoadCallback() {
                   @Override
                   public void onAdLoaded(@NonNull InterstitialAd interstitialAd) {
                           mInterstitialAd = interstitialAd;
mInterstitialAd.setFullScreenContentCallback(new
FullScreenContentCallback(){
                           @Override
                           public void onAdClicked() {}

                           @Override
                           public void onAdDismissedFullScreenContent() {
                               mInterstitialAd = null;
                               loadFullscreenAd();}

                           @Override
         public void onAdFailedToShowFullScreenContent(AdError adError) {
                               mInterstitialAd = null;}

                           @Override
                           public void onAdImpression() {
                           }

                           @Override
                           public void onAdShowedFullScreenContent() {
                           }
                       });
                   }

                   @Override
                   public void onAdFailedToLoad(@NonNull LoadAdError loadAdError) { super.onAdFailedToLoad(loadAdError);}
});
          }
// loadFullscreenAd

Step 3:
Main activity set content view এর পরে 

 new Thread(
            () -> {
  // Initialize the Google Mobile Ads SDK on a background thread.
       MobileAds.initialize(this, initializationStatus -> {});
        })
      .start();
এই লেখার পর নিচের লিখাটা লিখবো step 4

Step 4:

// FullScreen Ads
// Step 2 : Finding btnInterstitialAds and call InterstitialAds() method
Button btnInterstitialAds = findViewById(R.id.btnInterstitialAds);
loadFullscreenAd();

btnInterstitialAds.setOnClickListener(v -> {
   if (mInterstitialAd != null) {
       mInterstitialAd.show(MainActivity.this);
   }
});

Step 5:
<Button
   android:id="@+id/btnInterstitialAds"
   android:layout_width="match_parent"
   android:layout_height="wrap_content"
   android:text="Interstitial Ad button"
   />


//Log.d এটা হচ্ছে coder code এ ভুল আছে কিনা দেখতে পরবে এটা দিয়ে user এর কোনো কাজ নেই । তাই না রাখলেও অসুবিধা নাই।
Log.d("TAG", "The interstitial ad wasn't ready yet.");


ADMOB
Admob  এ যে নাম দিব ঐটা যাতে ভোটার id সাথে মিল থাকে ।

Setting>personal,account>information>test device সব পূরন করবো ।
Income শুরু হইলে payment option এ গিয়ে যাবতীয় information দিবো । 10$ হওয়ার পর mail করবে তারপর চিঠি পাঠাবে ঐ pin টা বসিয়ে information start করবো ।

App option এ গিয়ে app তৈরি / upload করবো ।

Play Store এ app upload দেওয়ার পর uniqid কাজ করে ।Appid=Adid

CLASS 32:- 9:00 MIN থেকে দেখো ।
CLASS 32.1:- কোথায় কোথায় ADD বসানো যাবে না ।
https://support.google.com/admob/answer/2936217?hl=en

App upload দেওয়ার আগে ভিডিওটা দেখবে । 

##Identity change :## 

App logo change

Package name change : 

Update version এ option টা নাই Package Name Change: Go Manifest > উপরে package(3rd/4th line) এ দেখো com. এর পর change

Java class এর সবার উপরে package এ দেখো com. এর পর change

Build.gradle.kts(Module:App) : ApplicationID থেকে com. এর পর change

Package name change risk  কারন অনেক সময় code উলোট পালট হয়ে যায় ।
এটার জন্য যা যা করতে হবে : 
Android থেকে project এ যাবো then 1st এর application name থেকে mouse right click : then Copy path > 
PC file a search করো : copy path এর location :Click search এর পাশের back button then will see the App file : Mouse Right :Send  to: Zipped file 

Shortcut app identity change : Android থেকে 3 dot এ যাবো > Tree Appearance > Compact Middle Factor unmark করো ।
Error আছে :  Java class  এ এবার 1st com.এর ভিতর  company name refactor : Rename: Rename Package: “Write new everything with small letter ” : : ✔ Search in comment  ✔ Search in text 
Select Project file option
দেখো একদম নিচে হাতের বামে Do Refactor এ click দেও

Same ভাবে App name ও করা যাবে ।

##App Name & Logo Change :## 
Name:: Go res folder: Values folder : String.xml folder : app name change
Logo:: Right Click app : New : Image asset :Foreground layout: path



##Open Developer Account:## 
সারাজীবনে Google 1 টা Developer account access দেয়। ভুলেও দুইটা খোলা যাবে না। যদি কোনো কারনে account ban হয়। তাহলে আপনার pc,mobile, mobile number,Router, A-Z change করে নতুন account open করতে হবে। বিষয়টা কতটা ভয়ঙ্কর। 

How to create google developer account : https://support.google.com/googleplay/android-developer/answer/6112435?hl=en

  
International dual currency card বানাও। একটা কার্ড দিয়ে আজীবন একটা account এর payment করা যাবে।
Islami bank dual currency debit card.
City bank account open করে পরে সেটাকে dual card এ তৈরি করা।

##App Bundle Create :##

Go Build :: Generate Signed App Bundle :: APK  ( Clinte  এর জন‍্য Apk )
jks file হচ্ছে security file.
এখানে choose existing মানে যখন আপনি update দিবেন তখন এটায় কাজ। আর প্রথমবার করলে  Create new. 
এরপর JKS location set করবা। 4 জায়গায় same password দিবে। এবং password এক জায়গায় লিখে রাখবে। তারপর আর option না choose করলেও হবে। ok.Next. এখানে 2 টা option debug ( App testing purpose) Release এটাই এখন use করবো। Create. 
password টা একটা text file এ save রাখবে।

এই File টাই Google এ upload দিবো।
App update দিলে build gradle  kts (Module App)  versionCode change করতে হবে। এটাকে প্রতিবার update এ এক করে বাড়াতে হবে। অথবা আগের থেকে পয়েন্ট হলেও বাড়াতে হবে। 
version name ও change হবে। আগের মতো same ভাবে আবার jks release করতে হবে।
Source code,jks file,password text file online এ কোনো যায়গায় save রাখবা। যেকোনো সময় তোমার pc crash করতেই পারে। Safe এ যাতে থাকে। 

Source code Zipp এ Convert ::
 File > Export > Export to Zip File>File Select >ok

Developer Policy ::
Developer Policy Center 
https://play.google/developer-content-policy/



##App Publish Basic setup :##

All apps থেকে Create app এ যাবো।App name : Language : App:Free:✅ : Create app

Grow : Main Store listing : App name : 





