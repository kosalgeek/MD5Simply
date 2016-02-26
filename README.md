# MD5Simply
``MD5Simply`` is simply a very simple tiny MD5 Encryption class for Android. You might find the same code all over the internet. But one big question remained: why DRY? So you don't have to create the same class yourself but simply use ``MD5Simply``. It is very useful to work with ``SharedPreferences``. And you see an example of using MD5 with ``SharedPreferences`` below.

# SETUP
1. Download MD5Simply.jar
2. Copy it and paste into your Android project at *App* > *libs* > right click on the jar file and choose *Add as Library*

# EXAMPLES
## Simple Example
```java
import com.kosalgeek.android.md5simply.MD5;

[...]

String yourText = "this is your normal text";
String md5Text = MD5.encrypt(yourText);
// that's it!
```

## Use MD5 with ``SharedPreferences``
```java
//Write Username and MD5 Password to SharedPreferences
SharedPreferences pref = getSharedPreferences("pref.txt", Context.MODE_PRIVATE);
SharedPreferences.Editor editor = pref.edit();
editor.putString("username", "oumsaokosal");
editor.putString("password", MD5.encrypt("kosalgeek"));
editor.apply();

[...]

//Read Username and Password from SharedPreferences
SharedPreferences pref = getSharedPreferences("pref.txt", Context.MODE_PRIVATE);
String username = pref.getString("username", "");
String password = pref.getString("password", "");
Log.d(TAG, username);
Log.d(TAG, password);

//Compare
String enteredUsername = "oumsaokosal";
String enteredPassword = "kosalgeek";
String md5Password = MD5.encrypt(enteredPassword);
if(enteredUsername.equals(username) && md5Password.equals(password)){
  Log.d(TAG, "same");
}
else{
  Log.d(TAG, "different");
}
//Of course, the result is "same"
```



## Follow Me
 * Get more free source code at https://github.com/kosalgeek
 * Watch my video tutorials at my YouTube channel https://youtube.com/user/oumsaokosal
 * Like my Facebook Page at https://facebook.com/kosalgeek
 * Follow me on Twitter https://twitter.com/okosal
 * Get more tutorials at http://www.kosalgeek.com and http://www.top12review.com
 
# LICENSE

(The MIT License)
Copyright (c) 2016 KosalGeek. (kosalgeek at gmail dot com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
