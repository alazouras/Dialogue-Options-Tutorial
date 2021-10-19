# Dialogue-Options-Tutorial
A tutorial on how to make multiple choice options in Unity



# 1) The Setup
To prep before getting the code in, first set up your scene and implement a text box and panel for the dialogue you choose from, like so:

![image](https://user-images.githubusercontent.com/91538155/137901533-100f7d48-50fa-4b2d-ac17-756fe5ac3546.png)

Then, change the default text to whatever you want the choice to be about, my example being this:

![image](https://user-images.githubusercontent.com/91538155/137902400-adce7f35-4973-43f3-92d5-c8fccfd81ca8.png)
![image](https://user-images.githubusercontent.com/91538155/137902413-9d73730a-aefa-4102-9f7f-a39f104dbb36.png)


# 2) Adding the options
For the options, we're gonna have three. So, for the first option, called Option01, create a button, make the tgext black and have the normal colour transparent. Then, you can fiddle with the colours for highlight, clicked and selected as you want to:

![image](https://user-images.githubusercontent.com/91538155/137903460-53a9a0d3-fb39-49fc-9489-92e8c5300fff.png)
![image](https://user-images.githubusercontent.com/91538155/137903427-74a9ba3c-2c99-4f00-a1a4-315e0634d020.png)

Once you've done the first button, copy and paste it twice more and have them be different dialogue choices with the same settings as Option01:

![image](https://user-images.githubusercontent.com/91538155/137904013-a412d3d7-8b8d-4b86-b1ad-e441c31d1f26.png)

# 3) The Actual Coding
First, create a script called ChoiceScript and open it up:

![image](https://user-images.githubusercontent.com/91538155/137904589-292d46b5-24fb-4b67-9371-f9401e70f401.png)

Then, add using UnityEngine.UI, and get rid of void start:

![image](https://user-images.githubusercontent.com/91538155/137904812-e6335615-9d3c-4491-b2b5-090d1e1f25ea.png)

Next, add the following Game Objects, which are, in order; The text box with the choice on it, one for each of the options, and a public int for when a choice is made:

![image](https://user-images.githubusercontent.com/91538155/137905345-b2daff04-fada-4e59-a91c-126044f8a86d.png)

Next, outside of void Update (which we're not using yet), create a public void for the first option:

![image](https://user-images.githubusercontent.com/91538155/137906451-7d3e9cee-8d05-4e63-8e24-f91e7c1fed23.png)

For this option, we then add the following, which will mean that the text in the text box will change to this specific line if option 1 is picked:

![image](https://user-images.githubusercontent.com/91538155/137912379-75c90819-eaeb-4237-bf82-1c5df6ee39a2.png)

Copy paste this public void for the other two options, and edit them where needed, as well as add different dialogue for each response:

![image](https://user-images.githubusercontent.com/91538155/137912889-0decdd5d-d94d-4409-bb20-7c322e0980cc.png)

Now, in void Update, add an if statement as shown here, and add the following:

![image](https://user-images.githubusercontent.com/91538155/137913582-fc023c4e-3c78-4da4-87d5-9221e6676da3.png)

# 4) Post-Code
Now, create an Empty Game Object and attach the code to it:

![image](https://user-images.githubusercontent.com/91538155/137913807-8389f061-1741-491b-9d5f-f4291b0797fd.png)

And fill in the options and text box:

![image](https://user-images.githubusercontent.com/91538155/137914013-efa9607f-2fa8-4efd-bf28-93f9a4a12fc1.png)

Now, we have to connect our actual buttons to the options. So to do that, open up each individual button and press plus in On Click ():

![image](https://user-images.githubusercontent.com/91538155/137914271-3955a94e-e0b5-4fe6-8541-56e458298d91.png)

And add your game object with the code in to each button and go into No Function, and change it to the script and then whichever option it is:

![image](https://user-images.githubusercontent.com/91538155/137914420-c44c0a3d-8518-49ff-a50a-eec5a4a37fc3.png)
![image](https://user-images.githubusercontent.com/91538155/137914577-33e475ee-7568-4af9-8de8-21dbdd122e0c.png)

# Congrats, it should work now!
