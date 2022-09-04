# This repository contains: 



1. A Gif searcher Fluttter application that request an external API that can shows trending gifs or searchers gifs.



# This project uses some of the following Flutter resources:

1. Navigator.push(context, MaterialPageRoyute) : used to change the page
2. GridView.Builder( ) : used to build a page with grid view
3. Image.network ( ): used to get images from internet
3. FadeInImage.memoryNetwork( ): used to load the image smoothly
4. Share.share( ): used to share content from application on social media
5. GestureDetector( ): used to turn the grid into a button
5. onSubmitted: 
5. CircularProgressIndicator ( ): used to create a movement on the loading icon



# This project uses the following external packages:



1. share_plus: ^4.0.10+1 : creates the button for sharing the gifs in other application as WhatsApp, gmail and others.

2. transparent_image: ^2.0.0

3. http: ^0.13.4: used to make a request on GIFS API

   



# This project uses the following external API's:



1. To search gifs : https://api.giphy.com/v1/gifs/search?api_key=LKLUdX9TvnkRni9IjtGUhEcXApGevGup&q=dogs&limit=25&offset=25&rating=g&lang=en
2. To show trending gifs: https://api.giphy.com/v1/gifs/trending?api_key=LKLUdX9TvnkRni9IjtGUhEcXApGevGup&limit=25&rating=g



# The lib's repository is organized as follows:



- **pages:** repo that contains inside the file home.dart.
  1. gif_page.dart
  2. home.dart


- **main.dart:** file that runs the application



# This project contains the following pages:



Number of pages: 2

1. Home. contains an AppBar, a gif searcer and a Grid that shows all the gifs of API
1. GifPage: this page is open whe the user clicks on a specific gif





# The user needs to enter the following data:



Home page:

1. There is a searcher field where user can enter some word so the application returns th gifs associated with that word. 



Gif Page:

1. The user dont need enter data on this page.





# This project contains the following ways to capture the data entered by the user. 



OnSubmitted:

1. There is no controllers in this project, it uses only onSubmitted parameter from textField widget to capture the data entered by user.

   





# This project contains the following models to receive the data entered by the user:





1. Map newToDo = {"**title**": "entered data added here" , "**ok**" : true or false}
   1. **title**: used to receive the entered description of a task
   2. **ok**: used to receive the status of completed task, that will be true when the task is completed and false when its not. 

2. Each "newToDo" will be added inside a list named  "todoList" that will store all the tasks added by the user.





# This project contains the following Lists to store all generated models:

1. Only the snapshot list obtained by the application request was used. . 



# This project persists data as follows:



1. This application does not persist data. 





# This project contains the following functions:



Void 


1. **int getItemCount**(List data): returns the length of list that will be used on GridView build. 



Futures - async

1. **Future < Map >  getGifs (.) async **:  makes request on the external API to get the gif datas that will be use on application

  

Widgets - returns

1. Widget **createGifTable(context, snapshot):** returns a widget that builds the grid visual for each gif inside the API.





# This project contains the additional variables:



1. **_search:** used to receive the word searched by the user
2. **_offset**: used to get new gifs from the API every time the user clicks the button to load more. 



# The Home page contains the following widget skeleton:

1. Scaffold

   1. appBar
   2. backgroundColor
   3. body
      1. Colum
         1. TextField
         2. FutureBuilder
            1. GridViewBuilder
               1. padding
               2. itemCount
               3. gridDelegate
                  1. SilverGridDelegateWithFixedCrossAxisAccount
                     1. crossAxisaccount: 2
                     2. crossAxisSpacing: 10
                     3. mainAxisSpacing: 10
                     4. ItemBuilder:
                        1. GestureDetector
   

   



