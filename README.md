
# Capstone: Music Positivity Analysis

## Presentation link: 
https://www.canva.com/design/DAFrE1Q6tQg/qBjzf98W6a-N4m_nTuvVJQ/view?utm_content=DAFrE1Q6tQg&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink

## Playlist link: 
https://open.spotify.com/playlist/2mfpY2nytL2xpQtci7y4Se?si=2dc1019cdfa54a26

### **Overview**

Music serves as a captivating medium that unites people with a shared interest. Its power lies in its ability to deeply resonate with our emotions, drawing out specific feelings depending on the genre we choose to embrace. For instance, heart-pumping genres like rock and EDM infuse us with energy and excitement through their fast tempos, while ambient melodies transport us to a more tranquil and reflective state.The profound connection between music and our emotions cannot be understated. It serves as a conduit for a plethora of feelings, from melancholy to anger, from joy to a myriad of emotions that lie somewhere in between. As a lover of music and someone who listens to music exclusviely onf Spotify to fit various moods, this concept intrigued me. This realization led me to delve into the transformation of musical positivity throughout history, exploring top hits from 1950 to 2022.

### **Data Question**

Which decade stands out as having the most positive music and what are possible influences that influenced a decase's positvity?

## **Methdologies:**

**Data Collection**

With the use of Python, I used Spotify's API to make multiple calls. Information requested was to include track name, artist, the track url, release year,the duration of the track and the tracks' audio features (danceability, tempo, energy, etc...).Defined Functions and loops were used to itterate through the requests of each playlists url, each request returned a dataframe with the requested information.This resulted in multiple API calls for 72 playlists, which produced over 6,300 tracks. Likewise Last.FM and Musicbrainz were used for additional information. Last.FM served as a genre checker for tracks that did not return a genre. Musicbrainz was utitlized to retrieve wheter the artist was a solo or group act as well as what the artists' gender.

**Cleaning the Data**

Data cleaning was needed for the genre and track title. Three genres were returned under the genre column. I used Excel formulas to remove uneeded characters from genre column entries, select the most frequent genre in the list as the sub genre. The inforamtion was then brought into Python to be organized into broader genres via user defined function using a loop to itterate through the sub genres. Additionally, artist names needed to be cleaned up as well. This was also done in Excel with formulas to remove unwanted characters and keep the first artist listed within the series of a column as the main artist (subsequent artist were artist featured on the track).

**Analyzing the Data**

After looking through the data. it was discoevered that metrics such as tempo, key, liveliness, and key had no correlations to the valence (positivity) score. The valence score was part of the audio features call to Spotify's API and was already calculated when the dataframe was returned. Only two metrics had (albeit weak) correlations to the valence score, danceability and energy. The analyais instead look at other possible influences on the valence score. The analysis focused on overall valence throughout time (1950-2022) and the possible influences from genre, artist type (group vs solo acts), song duration and artist gender. Groupby and other aggregations wre used in subsetting the data to retrieve the values needed to visualize the data.

**Visualizing the Data**

Matplolib and seaborn were utilized for line charts, scattersplots, and bar grapsh to create the primary visuals in Python. Data was then imported into PowerBi for additional line charts and bar graphs to beter show the relationship between valcnece scores and their corresponding decades. Power Bi was also used to show the dcline in valance for the most frequent genres.

## **Technologies**
Microsoft Excel
Python: pandas, numpy, matplotlib, seaborn
PowerBi-visuals

## **Data Sources**
- [Last.FM API](https://www.last.fm/api)
- [MusicBrainz API](https://musicbrainz.org/doc/MusicBrainz_API)
- [Spotify Web API](https://developer.spotify.com/documentation/web-api)

## **Conclusion**
Over the 72 year period of the top hits, we can see a steady decline in music positivity. Our music is not necessairly getting sadder, but it is getting less positive on average. The 1960's proved to be the most positive decade overall. This could be due to historical factors at that time (Civil Rights Movement,Vietnam War, etc... ).
From the analysis we can conclude:

-Reggae was the most positive genre on average

-Co-ed and Group acts faired better on average in regards to artist gender/artist type

-Shorter songs appear to have higher valence scores 

-The most frequent/popular genres are not the most positive

-The most positive decade in music was the 1960's