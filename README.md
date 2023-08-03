#joshua_capstone

**Nashville Software School Data Analytics Capstone**

**Overview**
Music serves as a captivating medium that unites people with a shared interest. Its power lies in its ability to deeply resonate with our emotions, drawing out specific feelings depending on the genre we choose to embrace. For instance, heart-pumping genres like rock and EDM infuse us with energy and excitement through their fast tempos, while ambient melodies transport us to a more tranquil and reflective state.The profound connection between music and our emotions cannot be understated. It serves as a conduit for a plethora of feelings, from melancholy to anger, from joy to a myriad of emotions that lie somewhere in between. This realization led me to delve into the transformation of musical positivity throughout history, exploring top hit songs from 1950 to 2022.

**Data Question**
Which decade stands out as having the most positive music?

**Methdologies**
With the use of Python, I used Spotify's API to make multiple calls. Information requested was to includes track name, artist, the track url, release date,the duration of the track and the tracks' audio features (danceability, tempo, energy, etc...).Defined Functions and loops were used to itterate through the requests of each playlists, each loop returned a dataframe with the requested information. Dataframes were organized with predefined columns upon loop completion. This resulted in multiple API calls for 72 playlists, which produced 6,300 tracks. Likewise Last.FM and Lyrics Genius API's were used for additional information. Last. FM served as a genre checker for tracks that did not return a genre. Lyrics Genius was used to gather the lyrics once the playlist tracks had been compiled into a dataframe. a lambda function was used to with a previously defined function to itterate through the dataframe to retrieve lyrics by matching track titles and artists.