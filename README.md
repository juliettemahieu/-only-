"# -only-" 
# Bank by Juliette Mahieu IOS2
***
## Description
This is an application to acces the database at that link *https://60102f166c21e10017050128.mockapi.io/labbbank/*.
Log in to acccess the application.
Read the /config data and the /accounts. 
Create new accounts with random information (just click on the button create and a new account is created, if you don't click on reload it will not appear on the list). 
The application is offline and you can load the information clicking on the button reload.
The first time the application will be lanch, no information will be save so the list are empty, but once you load, the information are safely saved in the phone and even if the application is close and reopen the information are keeped.



***
## Explain how you ensure user is the right one starting the app
I put a login system with simply a inputText where the user is ask to "Enter your password :".
The password is encrypted in the code, so the input that the user will enter will be encrypt too and then compare to the one saved in the code.
First I apply a very long key to the string to encrypt with Cipher.ENCRYPT_MODE, then I encrypt it in base 64.
Like that the password is not save in clear. 
There is a unique key only use to encrypt the password.


***
## How do you securely save user's data on your phone ?
The password is "EsilvMobile1".
With the same process in mind, I encrypt the data before I save it into **getSharedPreferences("sAccounts", getActivity().MODE_PRIVATE)** or **getSharedPreferences("sConfig", getActivity().MODE_PRIVATE)**.
Then when I read it every time I enter the activity, or when I reaload, I decrypt it using the exact same step but in DECRYPT_MODE. 
There is a unique key for saving the config data and one unique key for accounts data.
If the password entered is wrong, the inputfield is empty and an error message "Wrong password." appears. The users can try as long as he/she wants.


***
## How did you hide the API url ?
Like for the password or the data saved on the phone, I encrypt each url (*https://60102f166c21e10017050128.mockapi.io/labbbank/config* and *https://60102f166c21e10017050128.mockapi.io/labbbank/accounts*) with a key for each one and after pass it in base 64.



***
## Screenshot
![Image text](capture1.png)
![Image text](capture2.png)
![Image text](capture3.png)
![Image text](capture4.png)
![Image text](capture5.png)








