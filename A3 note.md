Start From 248
🔹 ১. PHP
Type: Server-side programming language
 Used for: Backend logic (e.g., login system, handling forms, database communication)
 ✅ Example Use: WordPress, Laravel, custom APIs
📌 PHP দিয়ে তুমি backend লিখতে পারো, তারপর সেটা দিয়ে MySQL ডাটাবেসে ডেটা রাখো বা Firebase-এর মত সার্ভিসে ডেটা পাঠাও।
🔹 ২. Firebase
Type: Backend-as-a-Service (BaaS)
 Used for: Realtime Database, Authentication, Hosting, Cloud Functions
 ✅ Example Use: Android/web apps with real-time chat or authentication
📌 Firebase নিজের মধ্যে authentication, database (NoSQL), analytics ইত্যাদি অনেক কিছু দেয় — কোন server লিখতে হয় না।
🔹 ৩. MySQL
Type: Relational Database
 Used for: Structured data storage with SQL queries
 ✅ Example Use: Store user profiles, product info, blog posts
📌 MySQL সাধারণত PHP, Python বা JavaScript দিয়ে query করে ব্যবহার করা হয়।
🔹 ৪. AWS (Amazon Web Services)
Type: Cloud Computing Platform
 Used for: Hosting servers, databases, storage, AI tools, etc.
 ✅ Example Use: Host a PHP app, run a MySQL database, use Firebase alternative like AWS Amplify
📌 AWS একটা cloud ecosystem — তুমি এখানে PHP server host করতে পারো, MySQL চালাতে পারো, Firebase-এর মত সার্ভিসও পাবে।

🔥 কোনটা কখন ব্যবহার করব?
🔧 যদি তুমি traditional web app বানাও → PHP + MySQL


📱 যদি তুমি Android/iOS app বানাও → Firebase


🌐 যদি বড় প্রজেক্ট, স্কেলেবল সার্ভার লাগে → AWS (with PHP/MySQL or Node.js, etc.)


🔁 যদি real-time feature দরকার হয় → Firebase Realtime DB / AWS AppSync



250 :
## Web Parsing by Volley Library

implementation 'com.android.volley:volley:1.2.1'

<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>

  Volley যে কোন একটা লিংকে হিট করে ওই লিংকে সকল তথ্য string আকারে নিয়ে আসে 


—-----------------------------------------------------------------------
Http link থাকলে Manifest এ  icon এর নিচে এইটা true করে দিতে হবে local ip দিয়ে host করলে ।

android:usesCleartextTraffic="true"


252
JSON(File Format ) 
Web এবং  App এর API তৈরি parsing করা। 
(Easy to Understand  for a coder) (Fast)(LightWeight)
.php এর মত হুবহু.json
এটা Hashmap এর মত key (Name) এর under এ value রাখা যায়। 
HashMap>>JSONObject (Row 1 টা || Column Unlimited )
Arraylist>>JSONArray (Row Unlimited || Column 1 টা )

—------ Row
|
|
|
|
Column 
253
Log.d(“Set finding keyword/tag in Logcat")
ডেভেলপাররা এইভাবে Log.d() ব্যবহার করে অ্যাপের বিভিন্ন অংশে কী ডেটা আসছে বা কী হচ্ছে, তা বুঝে নিতে পারেন — এটা সমস্যা খোঁজার জন্য অনেক সহায়ক।

255
Volley লাইব্রেরীতে String দিয়ে রিকোয়েস্ট করলে অনেক সময় বাংলা লেখা ভেঙ্গে যায় সেজন্য আমরা Array দিয়ে রিকোয়েস্ট করব ।

Log.d("serverRes",objectResponse.toString());
//objectResponse এটাতো একটা Object । String এ রুপান্তর করতে .toString() সাথে দিবো


  Log.d("MainActivity", "App started successfully");
"MainActivity": এটি একটি tag — আপনি আপনার ক্লাস বা ফিচারের নাম দিতে পারেন যাতে পরে খুঁজে পেতে সুবিধা হয়।


"App started successfully": এটি আপনার message, যেটা Logcat-এ দেখা যাবে।
[
JSON Array
]

{
JSON OBJECT
}

এক বা একাধিক OBJECT Array এর ভিতর রাখতে চাইলে শেষের টায় কমা দিব না 
[

   {
   },

   {
   },

   {
   }

]
262
একটা Database এ Data কিভাবে link এর মাধ্যমে Hit করে ? সেটা দেখবো । 
প্রথমে Data নামে(যেকোনো নাম দিতে পারো) c panel এ একটা PHP file create করলাম । তারপর সেখানে Database এর সাথে php connect করার code input দিলাম । তারপর ধরো link টা এমন হলো  https://nubsoft.xyz/data.php ।
এবার খেয়াল করো :  https://nubsoft.xyz/data.php?n=shahrear&m=01872000&e=arshahrear30  লক্ষ্য করো n এবং m এবং e এগুলো key । আর shahrear , 01872000 , arshahrear30 এগুলো হলো Values । তাহলে .php এর পর key=values এভাবে data input দিতে পারি । এখন এই link এ value গুলো update করলে আরেকটা database এ row create হয়ে data গুলো input হবে ।

264
ArrayList এর ভিতরে HashMap রাখি । আর Hashmap  এর ভিতর Key,Value রাখি

270
Http দিয়ে practice করার জন ্য270 number class 16 minute 16 sec থেকে দেখো 

271
## Fragment:
Fragment হলো Android-এর UI-র একটি অংশ। যেমন তোমার একটি অ্যাপে নিচে ট্যাব আছে — Home, Profile, Settings — এগুলো প্রত্যেকটা আলাদা fragment হতে পারে। প্রতিটি fragment আলাদা আলাদা XML layout ও Java কোড নিয়ে কাজ করে, কিন্তু সবগুলোই একটি Activity-র ভিতরে চলে।

Fragment আলাদা ক্লাস হয়, কিন্তু এক Activity-র ভিতরে চলে।
Layout আলাদা থাকে (fragment_xyz.xml)


res folder a Mouse Right Side Click > New > Fragment (Blank)

272
Fragment.java  তে mouse right click করবো Generate click Override Method click করলে Oncreate জিনিসগুলো Auto নেওয়া যাবে ।







276 : 
## Bottom Navigation Android

res folder a Mouse Right Side Click > New >Android Resource Directory > Resource type : menu >  তাহলে এবার আমরা দেখব menu নামে একটা ফোল্ডার তৈরি হয়ে গিয়েছে । এবার menu এর মধ্যে mouse right click দিবো > New > Menu Resource File>যেকোনো একটা নাম দেও । (Viz: bottom_nav_items)

Get Android Studio default icon : 
Drawable > New > Vector Asset >Clip art এ গিয়ে default icon নেও > icon Name দেও > Next > Finish

277 :
https://www.geeksforgeeks.org/android/how-to-align-navigation-drawer-and-its-elements-towards-the-left-or-right-of-the-screen-in-android/

https://github.com/arshahrear30/My-java-Note2022/blob/main/ima.jpg

 এখানে পুরো Red box কে ToolBar বলবো । বাম পাশের 3dot কে Navigation Drawer বলবো ।

ToolBar Use : 

CoordinatorLayout[  AppBarLayout[ ToolBar ]  ]

https://github.com/arshahrear30/My-java-Note2022/blob/main/ima.jpg

https://m2.material.io/components/app-bars-top#anatomy

এখানে উপরের হলুদ বক্স যেখানে সাধারনত profile রাখি এইটুকুকে header বলি । আর নিচে দেখো setting এর উপর একটা কালো দাগ এসে রয়েছে এটাকে devider বলি আর মাঝে যে Germany Australia Canada USA আছে এগুলোকে Menu item বলা হয় । devider আনার জন্য group group করে ভাগ করলেই হবে । 

283 :
## RecyclerView 
RecyclerView হল Android-এর একটি আধুনিক ও শক্তিশালী list view বা scrollable list দেখানোর উপায়। অনেকগুলো আইটেম (যেমনঃ নাম, ছবি, বাটন ইত্যাদি) যদি স্ক্রল করে দেখাতে হয়, তাহলে RecyclerView ব্যবহার করা হয়।

ListView = পুরনো, সীমিত ক্ষমতা
RecyclerView = নতুন, শক্তিশালী, highly customizable,Dynamic 

ListView দিয়ে সাধারণত ১০০ থেকে ৫০০ আইটেম নিয়ে কাজ করা যায় , তাহলে পারফরম্যান্স ভালো দেয় । এর বেশি আইটেম নিয়ে কাজ করলে এটি স্লো হয়ে যায় । সেজন্য আমরা RecyclerView  ইউজ করি আর এটি আনলিমিটেড আইটেম এর জন্য ব্যবহার করা যায় । এটি খুবই উন্নত এবং দ্রুত কাজ করে  ।  Facebook , Instagram  এ RecyclerView use হয় । 

284 :

picasso dependency এর পরিবর্তে bumptech/glide library ব্যবহার করি । 11:00min class done








