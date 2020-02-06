# How are the features of the song are different in the world?

## Introduction and related work
Make an analysis on how the song's features are different in different country can be done for many reason. An example can be for the artists, they can understand better where them song can be successful and so where put much effort. It can also be helpful for the users to understand in which country they are more belong and if his tastes music is similar to the people of him country.

About this data-drive question we have found a related [project](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5350199/) of the 2017, the big problem of this project is that the dataset choose doesn't have the features about the song that nowdays spotify give us.

## Ecploratory data analysis
This give us the opportunity to make analysis on what the people are listening, in particular we want to concetrated on how the features are going to caratestic a country. For example we all know that the song that are listening in the latin america country are more danceable than for example the north european country like Norway,Sweden and Finland.
Our analysis has been done with the using of the Spotify API, in particular we have used the *spotifyr* package of R to access on it. We have decide to concentrate our anlysis on some specific features:

- **danceablity**: It describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. More higher is the value more the song is danceable.
- **energy**: Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.
- **valence**: Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry)
- **tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.

We have choose this following features on which make the analysis because are the one with the large devation standard,so where we can found a real difference between the countries. All the select features are between the value 0 and 1 (except for tempo), and seem that are following a normal distribution (as you can see from this [link](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/)).

I have used a dataset obtain from the merging of all datasets of [spotify ranking](https://spotifycharts.com/regional) per countries of the 17th December 2019. For each feature we get a mean of the value on the top 200 per each country and we are going to use the mean to rapresent a country.

For the rapresentation of the features we have decided to use the world data map, that type of visualization for this question is actually perfect. This graph can show us if the neighbour share the same type of taste in general. For showing of the feature on the country we have used scale made by the function viridis in R that is helpful to make the data seems more uniform. This scale is perfect because show hot color for represent the features of the hot song, while for the cold song use cold color.

![alt text](Rplot07.svg)

From the four graph we can assume that the Latin America seems the state with the more happy and danceable song, while in Europe we note a consistent difference between the South Countries and the North Countries, the South ones tends to be more similar to the Latin America while the North's songs seem more cold. We can note that the North American Countries tends to have the same taste of the Australia and New Zealand, obviously more cold taste than the spanish song but not like North European ones. About the Asia countries the India seems to have his particular taste, while the Indonesian ones seem to share the same taste about music.

