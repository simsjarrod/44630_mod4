# Requests, JSON, and basic NLP with spaCy

Complete the tasks in the Python Notebook in this repository.
To be submitted for credit, all changes must be committed and pushed to this repository (do not create your own repository unless instructed to on the course website).

### Rubric

* (Question 1) Lyrics printed: 1 pt
* (Question 1) File created and submitted with notebook: 1 pt
* (Question 2) Correct polarity reported: 1 pt
* (Question 2) Question answered thoughtfully: 1 pt
* (Question 3) Function defined as specified: 1 pt
* (Question 3) Song lyrics retrieved and stored in separate files (0.5 pts/song): 2 pts
* (Question 4) Polarity scores printed (with appropriate label containing song title, .25 pts/song): 1 pt
* (Question 4) Questions answered thoughtfully: 2 pts

### Objectives
This exercise illustrates how to access web-hosted APIs, get back a response in JSONLinks to an external site. format, and extract the information we need from the JSON. Accessing APIs is a key skill for data analysts. We can use web APIs to get stock data, weather data, and much more. We'll use an API to access song lyrics or poems in this exercise. We don't care which API - there are many and they change. The skill skills are being able to (a) make an API request and (b) find the information we need in the returned response. 

Helpful Hint: You can make a simple API request directly in your browser to test it BEFORE making the same request from your notebook or script.

### Important: Use a Different API
The current instructions are no longer working. APIs are notorious for changing out from under us. The provided link no longer returns lyrics. 

There are other ways to get song-lyric or poem data in JSON format. Any lyrics or poem data in JSON format will do. To proceed:

* Try this instead: https://gist.github.com/neloe/e38e4d3283418e096aac80fa48bb66bd Instead of author/poem, use artist/song to fetch your content.
* Or try this:  lyricsgenius · PyPI. The site gives good instructions. When you create JSON documents it pulls everything from the search for the song, so  just manually go through and find the lyrics and delete the rest.  You have to create an access token for it to work. 
* Or this - provide a value for the variables artist and song - inspect the result (you'll need to convert xml to json): 
 result = requests.get('http://api.chartlyrics.com/apiv1.asmx/SearchLyricDirect?artist='+artist+'&song='+song).text
Then

* Review these examples to learn how easy it is to access public APIs from Python.
* Check out: https://github.com/public-apis/public-apis. to explore other free public APIs.
Web requests are key skills in data mining. Don't miss out!  

### Important: Working With Web Information
Always print/display the results you get back to your screen.
If you get a list (it will be enclosed in square brackets []), take a single item from the list (usually lst[0]).
If the lyrics are nested, get only the part of the response needed, e.g., lst[0]['lines']. 
The actual process to get the necessary information varies by API - get used to using print on EVERYTHING while setting up your code, and then comment out or delete unneeded print statements - once you know the "shape" of every step. 
The API not working is common -  we can expect that in our field. The ability to proceed in the face of challenges is part of our value. Use any school-appropriate lyrics - or poems - it's best to find something that engages you, but please be mindful of your audience. Use your professional judgement. 

### Important: Question 3 - Writing Custom Functions
For question 3, write a custom function that takes three parameters:  artist / song / filename you'll write the JSON to.  A good function name might be write_song_from_api_to_json() – seriously – it’s super reusable and you’re hard coding the API you choose, so it makes sense - you can even name it specific to the api you're calling as that is likely the only response on which it will work. 

The filename passed in will be the name of the file you’re writing the JSON to locally  (with the lyrics or poem result returned). It should make a new file on your machine in the same folder as your notebook, with the file name passed into the function. (e.g., passing in “the-night-santa-went-crazy." would write to a file named "the-night-santa-went-crazy.json". You could require the .json extension in the argument, or you could append the .json in your function.)

You want to write a nice, reusable function you can call four times, and each time it will create a new JSON file with a .json file extension.  This actually showcases several valuable skills - the ability to call an API and the ability to write a custom function - show off what you can do! See our FAQ for more help. 

Some machines hide file extensions from us – make sure you can see your file extensions (e.g., .json, .ipynb) as well as the file name.

### Task 1. Get Started
1. Copy the base repository into your GitHub account by selecting the "Use this Template" button on GitHub and specifying yourself as the owner.  The base repository is available at: https://github.com/wmnlp-materials/json-sentimentLinks to an external site.
2. Clone YOUR new repo down to your machine.
 

### Task 2. Open Notebook and Complete Tasks 
1. On your machine, open the Jupyter Notebook for editing. 
2. Required: In your Markdown introduction, add a viewable, clickable link to your GitHub repo after your name. Build your brand and make your Markdown introduction clear and professional. 
3. Required: Use Markdown headings  (e.g. Question 1) to clearly show your content by each question number. 
4. Complete the first task.
5. Execute the notebook. Commit and push to GitHub. Verify your notebook appears correctly.
6. Complete the second task.
7. Execute the notebook. Commit and push to GitHub. Verify your notebook appears correctly.
8. Work this way until all tasks have been completed. 
 

### Task 3. Export to HTML and Finalize Repo
1. Execute each notebook.
2. After executing, export each notebook to HTML.
3. Commit and push your HTML files to your GitHub repo along with the executed notebooks. 
4. Verify you have a professional README.md that introduces your GitHub repository and provides helpful information about your project. 
Note: Your instructor may review just the notebooks - or just the HTML. Either way, notebooks are web pages, and we are learning to mine web pages. The more familiar you are with web pages, the easier it will be to get the information you need. 

### Requirements
1. Markdown introduction with name and clickable link is required.
2. nMarkdown Section Headings for each Question are required. 
3. Execute your code before exporting HTML and pushing notebooks. (See FAQ for help.)  
4. Unexecuted code is not eligible for credit.
5. See Project Submission Instructions

### Reflections (on your own)
These are key skills for gathering information from the web. It's not easy, but it's very useful. 
* What is JSON?
* What is sentiment analysis?
* How popular are these libraries?
* How often do things change on the web?
* What can go wrong when using APIs?
* * Being able to find a new source of information and use the published API is a key skill and widely needed. 
* Not everyone will endure the frustration to learn continously.
* Do you find challenges engaging?
* We get paid to deal with things that many others will not. 
* The payoff when getting things to work can be pretty rewarding.
* The ability to figure things out is quite valuable. 
* Take a moment to appreciate all the skills and traits that go into success in this field. 