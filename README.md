# How-to-see-logcat

## How about finding your error by yourself ?

## Solution:-

The best way to learn is to solve problem by yourself. Here I'll tell you how to proceed when your app crashes suddenly and you have no idea.

If your application crashes then we'll be looking for " logcat ".

 ### What is logcat ?
  
  Logcat is a command-line tool that dumps a log of system messages, including stack traces when the device throws an error and messages that you have written from your app with the Log class. 
    
   For more  https://developer.android.com/studio/command-line/logcat.html
  

          
###  a) You will find logcat at the bottom of your Android Studio Screen.


![logcat](https://user-images.githubusercontent.com/25812257/37620112-580c5e1e-2be1-11e8-91b1-32f42b4662f9.PNG)


###  b) Click "logcat" and  there you will see lot of messages(logs).

![logcat2](https://user-images.githubusercontent.com/25812257/37625346-8e1b5662-2bf1-11e8-954f-1421c2958318.PNG)


### c) Next step is to filter our logcat to error mode so that we can see only those message which are related to error. Change your logcat from verbose to error mode and here is your logcat for error.


![errormode](https://user-images.githubusercontent.com/25812257/37625352-93477846-2bf1-11e8-9128-72374b4d070b.PNG)


Great!! now you know how to open logcat. Now let's learn how to use logcat.

Let's take an example.  The Below program converts two string numbers into integers, calculates the sum and prints the result in TextView as you can see the layout.xml below.. but to learn how to use logcat I have made mistake in this code..Let's resolve the error by seeing the logcat. 


#####  MainActivity.java

![example](https://user-images.githubusercontent.com/25812257/37626546-74bca5ae-2bf6-11e8-8e0f-0050c3c631d8.PNG)

#####  activity_main.xml

![resultlayout](https://user-images.githubusercontent.com/25812257/37626573-9c65761c-2bf6-11e8-8e47-04868a1354c4.PNG)

But when we run the program, our program will crash so we'll open the logcat as we're told above.[Note : If you're using external device to run the app then it must remain conntectd to your android studio].The logcat for above example looks like :- 

![ssdfg](https://user-images.githubusercontent.com/25812257/37626899-eaf702fe-2bf7-11e8-8700-305b0cd09b23.PNG)



   We will look only for the highlighted lines in logcat...we can see that logcat specifies error like "NumbeFormatException"...and also we see ' Invalid int: "abc" ' ,with a error of "NumbeFormatException" and ' Invalid int: "abc" ' we can guess that error is related to NumberConversion and also there is something wrong with int ...and you can see that these error occur in the Mainactivity.java by looking the path in the first line. So, we'll move back to MainActivity.java
  
  
 #### Mainactivity.java
 
 ![dfs](https://user-images.githubusercontent.com/25812257/37627349-fdf68d78-2bf9-11e8-9a26-8af78b1c1a45.PNG)
 
 
 Now, we'll look our Mainactivity.java. Here you see that, we're not taking integers string for s1 so while parsing that string into integers, it creates error.
 
 ####  Tip :- Sometimes your logcat might not be easy to understand, or can more complex as compared to this example and you might not have any  idea about the error, so in that case just copy the highlighted lines of your logcat and paste on google and in many cases you will get your solution on stack-overflow
 
                                                                
 ##### Special thanks to :- 
 - FlyingKripto -[Github](https://github.com/FLYINGKRIPTO/)
