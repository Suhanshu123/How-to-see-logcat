# How-to-see-logcat

## 17. How about finding your error by yourself ?

## Solution:-

The best way to learn is by solving your problem by yourself. Here I'll tell you how to proceed when your app crash suddenly.
If your application crash then follow below steps and you'll get to know where your error comes from :

### 1- First checkout your logcat. Don't know about logcat- Not worry just follow the steps:-
       
  Logcat is a command-line tool that dumps a log of system messages, including stack traces when the device throws an error and messages that you have written from your app with the Log class. [Definition by :- https://developer.android.com/studio/command-line/logcat.html ]
         
####  a) You can find logcat in the bottom of your Android Screen.


![logcat](https://user-images.githubusercontent.com/25812257/37620112-580c5e1e-2be1-11e8-91b1-32f42b4662f9.PNG)


####  b) Click "logcat" and  there u see lot of messages.

![logcat2](https://user-images.githubusercontent.com/25812257/37625346-8e1b5662-2bf1-11e8-954f-1421c2958318.PNG)


####  c) Next step is to filter our logcat to error mode so that we can see only those message which are related to error.Change your logcat from verbose to error mode.


![errormode](https://user-images.githubusercontent.com/25812257/37625352-93477846-2bf1-11e8-9128-72374b4d070b.PNG)


Now, we'll do practice on the below example. The program  converts two string numbers into integers and then calculating the sum and then printing the result into the textView as you can see the layout.xml.


#####  MainActivity.java

![example](https://user-images.githubusercontent.com/25812257/37626546-74bca5ae-2bf6-11e8-8e0f-0050c3c631d8.PNG)

#####  activity_main.xml

![resultlayout](https://user-images.githubusercontent.com/25812257/37626573-9c65761c-2bf6-11e8-8e47-04868a1354c4.PNG)

But when we run the program, our program will crash so we'll open the logcat as we're told above. The logcat for above example looks like :- 

![ssdfg](https://user-images.githubusercontent.com/25812257/37626899-eaf702fe-2bf7-11e8-8700-305b0cd09b23.PNG)

###  Great now you learn how to open logcat. Now question arises how to see logcat.

  We will look after only the highlighted lines in the every logcat...if you see those highlighted lined then you can see that error  is related to "NumbeFormatException"...and also you see "abc" ;with a little knowledge of "NumbeFormatException" you can think that something is related to NumberConversion and also there is something wrong about "abc" ...and you can see that these error occur in the Mainactivity.java. So, we'll move to MainActivity.java
  
  
 #### Mainactivity.java
 
 ![dfs](https://user-images.githubusercontent.com/25812257/37627349-fdf68d78-2bf9-11e8-9a26-8af78b1c1a45.PNG)
 
 
 Here you see that, we're not taking integers string for s1 so while parsing that string into integers in creates error.
 
 ###  Tips :- Sometimes your logcat is not as clear or more complex as compare to this example so in that case we'll copy that lines and paste into google and in many cases first link is of stack-overflow and you will get answer of many questions.
