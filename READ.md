# AdmissionPedia-Laravel
One of the most complex web projects I have ever done. This project is intended for the admission examinee student's of Bangladesh.
The can easily find out their suitable universities based on their GPA.
Also they can create a great community by creating post, replying and many more.

To run or deploy this project please follow the instruction
## Instruction
This is a laravel project. So first install all the necessary laravel dependencies.

Load admissionpedia_university.sql in xampp or any mySql Database.
Okay So you have installed all the dependencies.And also you have started your project by this IP :localhost:8000 

First of all, all the databases are pretty much empty. 
The website can only process HSC examinee --> Science Department students only. Also Foreign students can submit
their SAT score and find suitable universities.You can submit your GPA or scores in 'Find the best univesity'.

But you will find empty result because all the databases are empty. So you have to login as admin.To login click 'Community'
This website uses email verification system. I will come to this part later. You can login with these credentials
also :   email  : asd@asd   password : asd.

Upon your login go to 'Add univesity'. Here you can add any universities along with their requirments. I am breaking this part by part.
First submit univerity full name then just short name. Then submit number of total units in that university.
Next part comes about defining the unit names or Unit Description. I am giving you an example.

Suppose the varsity full name is Shahjalal university of Science and Technology. Short name is : SUST. Unit : 3 units in total.
They have three units : A for Commerce student , B for Science students, C unit where every one can apply.So 
in Unit Description you write like this :  ' A:C,B:S,C:A ' [without apostrophe] This means A goes to Commerce, B goes to Science and C goes to All. These unit will show up when someone submit their GPA. 
For BUET their are only two units : Ka and Kha both for Science student. Fill the Unit description like this :
' Ka:S,Kha:S '

Now fill up 'Total seat,' 'Apply start date', 'Apply off date', 'Required SSC GPA' ,  'Required HSC GPA' ,
'Required Total GPA ' one by one.
Engineering Universities demand aggregate GPA of Bangla + English + Physics + Math + Chemestry. If any 
university like DU,SUST does not require this kind of aggregate GPA then fill it with 0.
SUST, DU deducts a portion of mark based on GPA. Fill it with that. 
Some universities accept SAT score. If any univeristy does not accept SAT score fill it with 9999.


Now to edit Unit of any particular universities 'Edit University Details'. Here is no more complexity.
You can read and also understand what to do. 

Many universities like DU, SUST they require GPA for units even for some subjects. Like SUST CSE requires
3.5 GPA in Math at least. So every information must be fed accordingly in 'Edit Unit Details'


The project uses Email verification system. To set email verification system open .env file which is located in 
university admissionpedia.Scroll down and find these :

	MAIL_DRIVER=smtp
	MAIL_HOST=smtp.mailtrap.io
	MAIL_PORT=2525
	MAIL_USERNAME=null
	MAIL_PASSWORD=null
	MAIL_ENCRYPTION=null

	
Change according like this : 

	MAIL_DRIVER=smtp
	MAIL_HOST=smtp.gmail.com
	MAIL_PORT=465
	MAIL_USERNAME=Your email
	MAIL_PASSWORD=email password [No apostrophe]
	MAIL_ENCRYPTION=ssl
	
If you have router then you have to port forward 465. Please google how to port forward according to your router config. If you do not want to take these kind of hassle just login with default credentials and then 
'Add New member.'



If you face any kind of bugs or issues feel free to email me : ahmedyunuspilot@gmail.com.

******************************************** Happy Coding ********************************************

