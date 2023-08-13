
# Music Positivity Capstone: "Are You Happy Now?"

### **</u>Overview**

Music serves as a captivating medium that unites people with a shared interest. Its power lies in its ability to deeply resonate with our emotions, drawing out specific feelings depending on the genre we choose to embrace. For instance, heart-pumping genres like rock and EDM infuse us with energy and excitement through their fast tempos, while ambient melodies transport us to a more tranquil and reflective state.The profound connection between music and our emotions cannot be understated. It serves as a conduit for a plethora of feelings, from melancholy to anger, from joy to a myriad of emotions that lie somewhere in between. This realization led me to delve into the transformation of musical positivity throughout history, exploring top hit songs from 1950 to 2022.

### **Data Question**

Which decade stands out as having the most positive music?

## **Methdologies:**

**Data Collection**

With the use of Python, I used Spotify's API to make multiple calls. Information requested was to include track name, artist, the track url, release year,the duration of the track and the tracks' audio features (danceability, tempo, energy, etc...).Defined Functions and loops were used to itterate through the requests of each playlists url, each loop returned a dataframe with the requested information. Dataframes were organized with predefined columns upon loop completion. This resulted in multiple API calls for 72 playlists, which produced over 6,300 tracks. Likewise Last.FM and Lyrics Genius API's were used for additional information. Last. FM served as a genre checker for tracks that did not return a genre. Lyrics Genius was used to gather the available lyrics once the playlist tracks had been compiled into a dataframe and organized for analysis.

**Cleaning the Data**

Data cleaning was needed for the genre and track title. Three genres were returned under the genre column. I used Excel formulas to remove uneeded characters from genre column entries, select the most frequent genre in the list as the sub genre. The inforamtion was then brought into Python to be organized into broader genres via user defined function using a loop to itterate through the sub genres. Additionally, artist names needed to be cleaned up as well. This was also done in Excel with formulas to remove unwanted characters and keep the first artist listed within the series of a column as the main artist (subsequent artist were artist featured on the track).

**Analyzing the Data**
After looking through the data, I saw that there were over 6,300 songs in across the 72 playlist the that wever retrieved from Spotify's API. It was discoevered that metrics such as tempo, key, liveliness, and key had no correlations to the valence (positivity) score. Only two metrics had (albeit weak) correlations to the valence score, danceability and energy. The analyais instead look at other possible influences on the valence score. The analysis focused on overall valence throughout time (1950-2022) and the possible influences from genre, artist type (group vs solo acts), song duration and artist gender.