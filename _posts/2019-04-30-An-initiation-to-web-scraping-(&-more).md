---
description: "Let's talk about Electro music. And Web Scraping."
comments: true
---    
<br><br>
<center>
    <img src="{{ site.baseurl }}/images/ElectroPhilarmoniedeParis2019-1.jpg" alt="Expo Electro at the Philarmonie de Paris, summer 2019" height="auto" width="150">
</center>  
<br>
>Electro music was inspired by House music, which was born in the 1980's in Chicago. Its name comes from the "Warehouse", the club where DJ Frankie Knuckles invented the style.
<br>
## Why learn web scraping?  

I love electro & house music, and have always wanted to have all the upcoming music festivals (worldwide) effortlessly show up in my Google Calendar, so that I could simply pick my next travel destination according to where the best events would be taking place.  

The thing is, since Google's Public Calendars were depleted[<a href="#1dn" class="footnote" id="1up"><sup>1</sup></a>](#1dn), I haven't been able to find a practical solution that would allow me to easily (automatically) add (hundreds to thousands of) events to my calendar.  

Say, if I wanted to add all the upcoming electro festivals worldwide (hundreds) already listed on my favorite website, I would have to do it manually, and this would take hours if not days.  

I had heard about scraping in the past, which allows to quickly extract data from websites, and I knew I could somehow use Google Calendar's API to add events to my calendar using code. That's all I needed to get started.  
<br><br>

## How I went about it:    

**Step #1:** finding reliable, well maintained Events listings 🌍⬅💻🧐  
Tools: [`Google search`](https://www.google.com/), friends' recommendations.  
How: I made a shortlist of websites which were fairly important, regularly maintained, with the most events listed and with the most detailed information per event. I ended up choosing one single website.    

**Step #2:** (_respectfully_) scraping the Events listing 🌍➡💻🤔  
Tools: [`Python`](https://www.python.org/), [`Scrapy`](https://scrapy.org/), [`Virtual Environments`](https://www.pythonforbeginners.com/basics/how-to-use-python-virtualenv/).  
How: I wrote a Python script using Scrapy, a Python framework which made it easy to extract data about 1500+ events from the website, while storing it all neatly in a csv file, all in just a few seconds. 
Note that by respectfully, I mean that some websites do not wish to be scraped, Scrapy automatically pays attention to this by checking the websites' "robot.txt" file.

**Step #3:** Adding events from a CSV file to my Google Calendar 📅⬅💻😁  
Tools: [`Python`](https://www.python.org/), [`Pandas`](https://pandas.pydata.org/), [`Google Calendar API`](https://developers.google.com/calendar/).  
How: I wrote another Python script, this time to extract the data from the csv file and upload it to my Google Calendar using its API (I find the tutorial videos very handy). I also added code to update existing events every time I run the program. Pandas, a Python data analysis library, was extremely convenient to structure and play with the data.  
<br><br>
<center>
    <figure class="video_container">
      <video allowfullscreen muted autoplay loop poster="{{ site.baseurl }}/images/festoches.png" width="150">
        <source src="{{ site.baseurl }}/images/festoches.m4v" type="video/mp4">
      </video>
    </figure>
</center>
<br><br>

## Bottom line:

In just about 2 days, I was able to write code which allows me to fill and easily update a Calendar containing hundreds (1500+) of upcoming electro and deep house festivals worldwide over the next 24 months, which I can easily share with friends.

I now have a clear view of all upcoming festivals and sure am going to pick my next trips according to some of the events I'll see pop up in my calendar a few weeks to months ahead.

I'll see how handy this Calendar proves to be, in the meantime I have learnt a lot about Python, scraping and APIs.

****

<footnote>
    <a href="#1up" class="footnote" id="1dn">1.</a> Google public calendars: somewhere around 2009, unmaintained public user calendars actually brought Google more blame than praise from its users so Google decided to end the project.
</footnote>