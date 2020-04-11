# hiuwing0107-Assignment9-CISC3140
## Objective: Connect to an API end point of NASA Picture of the Day and display the information from the API in nicely   formatted way

### Access data from an API end point in https://postwoman.io/ to preview the response from a HTTP GET request

    GET: https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY

{
  "copyright": "Antonio\nFinazzi",
  "date": "2020-04-11",
  "explanation": "Shared around world in early April skies Venus, our brilliant evening star, wandered across the face of the        lovely Pleiades star cluster. This timelapse image follows the path of the inner planet during the beautiful conjunction showing its daily approach to the stars of the Seven Sisters. From a composite of tracked exposures made with a telephoto lens, the field of view is also appropriate for binocular equipped skygazers. While the star cluster and planet were easily seen with the naked-eye, the spiky appearance of our sister planet in the picture is the result of a diffraction pattern produced by the camera's lens. All images were taken from a home garden in Chiuduno, Bergamo, Lombardy, Italy, fortunate in good weather and clear spring nights.   Notable APOD Submissions: Gallery of Venus passing in front of the Pleiades",
  "hdurl": "https://apod.nasa.gov/apod/image/2004/TimelapseVenusPleiadesFinazzi.jpg",
  "media_type": "image",
  "service_version": "v1",
  "title": "Venus and the Pleiades in April",
  "url": "https://apod.nasa.gov/apod/image/2004/TimelapseVenusPleiadesFinazzi800.jpg"
}

### Picture of the day
    https://apod.nasa.gov/apod/ap200404.html

### Parse the data, which requires understanding their data structures

    //add a new key in Parameters (date 2020-04-04)

      Parameters list
      ?api_key=DEMO_KEY&date=2020-04-04
      date : 2020-04-04

{
  "copyright": "Fred Espenak",
  "date": "2020-04-04",
  "explanation": "After wandering about as far from the Sun on the sky as Venus can get, the brilliant evening star is crossing paths with the sister stars of the Pleiades cluster. Look west after sunset and you can share the ongoing conjunction with skygazers around the world. Taken on April 2, this celestial group photo captures the view from Portal, Arizona, USA. Even bright naked-eye Pleiades stars prove to be much fainter than Venus though. Apparent in deeper telescopic images, the cluster's dusty surroundings and familiar bluish reflection nebulae aren't quite visible, while brighter Venus itself is almost overwhelming in the single exposure. And while Venus and the Sisters do look a little star-crossed, their spiky appearance is the diffraction pattern caused by multiple leaves in the aperture of the telephoto lens. The last similar conjunction of Venus and Pleiades occurred nearly 8 years ago.",
  "hdurl": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg",
  "media_type": "image",
  "service_version": "v1",
  "title": "Venus and the Sisters",
  "url": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg"
}

    //add a new key in Parameters (hd true)

      Parameters list
      ?api_key=DEMO_KEY&date=2020-04-04&hd=true
      hd true
      
{
  "copyright": "Fred Espenak",
  "date": "2020-04-04",
  "explanation": "After wandering about as far from the Sun on the sky as Venus can get, the brilliant evening star is crossing paths with the sister stars of the Pleiades cluster. Look west after sunset and you can share the ongoing conjunction with skygazers around the world. Taken on April 2, this celestial group photo captures the view from Portal, Arizona, USA. Even bright naked-eye Pleiades stars prove to be much fainter than Venus though. Apparent in deeper telescopic images, the cluster's dusty surroundings and familiar bluish reflection nebulae aren't quite visible, while brighter Venus itself is almost overwhelming in the single exposure. And while Venus and the Sisters do look a little star-crossed, their spiky appearance is the diffraction pattern caused by multiple leaves in the aperture of the telephoto lens. The last similar conjunction of Venus and Pleiades occurred nearly 8 years ago.",
  "hdurl": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg",
  "media_type": "image",
  "service_version": "v1",
  "title": "Venus and the Sisters",
  "url": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg"
}

### Parse out specific values (&date=2020-04-04) to display as html web page 

    https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY&date=2020-04-04

{
  "copyright": "Fred Espenak",
  "date": "2020-04-04",
  "explanation": "After wandering about as far from the Sun on the sky as Venus can get, the brilliant evening star is crossing paths with the sister stars of the Pleiades cluster. Look west after sunset and you can share the ongoing conjunction with skygazers around the world. Taken on April 2, this celestial group photo captures the view from Portal, Arizona, USA. Even bright naked-eye Pleiades stars prove to be much fainter than Venus though. Apparent in deeper telescopic images, the cluster's dusty surroundings and familiar bluish reflection nebulae aren't quite visible, while brighter Venus itself is almost overwhelming in the single exposure. And while Venus and the Sisters do look a little star-crossed, their spiky appearance is the diffraction pattern caused by multiple leaves in the aperture of the telephoto lens. The last similar conjunction of Venus and Pleiades occurred nearly 8 years ago.",
  "hdurl": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg",
  "media_type": "image",
  "service_version": "v1",
  "title": "Venus and the Sisters",
  "url": "https://apod.nasa.gov/apod/image/2004/VenusM45-2020Apr02-105x.jpg"
}

-------------------------------------------------------------------------------------------------------------------------
CISC 3140 - Design and Implementation

Professor: Katherine Chuang

Student Name: Hiu Wing, Lam

Emplid: 23626630

Assignment 9 - API Client
