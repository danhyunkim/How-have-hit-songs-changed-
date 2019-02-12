# Executive Summary

An analysis of popular hit songs from 2008, 2013 and 2018. 

## Problem Statement

Which audio features have the most influence on making a hit song?

Who can this benefit?

- **Record labels and independent artists!**

## Data Collection

- Web Scrape: 

	- BillBoard Year-End Hot 100 Songs (2008, 2013, 2018)
	- SongFacts (2008, 2013, 2018)

- Interface with API:

	- Genius - song lyrics 
	- Spotify - audio features

### Data Dictionary

**Audio Features**

|Key|Value Type|Value Description|
|---|---|---|
|song|string|Title of the song.|
|danceability|float|Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.|
|energy|float|Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.|
|key|int|The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.|
|loudness|float|The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.|
|mode|int|Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.|
|speechiness|float|Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.|
|acousticness|float|A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|instrumentalness|float|Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.|
|liveness|float|Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.|
|valence|float|A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).|
|tempo|float|The overall estimated tempo of a track in beats per minute (BPM).|
|duration_sec|float|The duration of the track in seconds.|
|time_signature|int|An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).|
|hit|int|1 if a song is a hit (popular) song and 0 if not.|

**Dropped Columns**

|Key|Value Type|Value Description|
|---|---|---|
|Unnamed: 0|int|Index from csv|
|type|string|The object type: “audio_features”|
|id|string|The Spotify ID for the track.|
|uri|string|The Spotify URI for the track.|
|track_href|string|A link to the Web API endpoint providing full details of the track.|
|analysis_url|string|An HTTP URL to access the full audio analysis of this track. An access token is required to access this data.|
|duration_ms|int|The duration of the track in milliseconds.

## Modeling

**Audio Features:**

- Neural Network 
- Logistic Regresssion

**Lyrics:**

- Logistic Regression

## Results, Findings & Recommendation

**Model Results:**

Audio Features:

- Accuracy score: 0.628
- Recall score: 0.623

Lyrics:

- Accuracy score: 0.939
- Recall score: 0.08

**Findings**

Loudness and danceability have the biggest influence on whether a song is a hit. Energy and instrumentalness have the smallest influence.

**Recommendation**

Invest in creating louder songs that have upbeat tempos and strong beats that are ideal for dancing!

## Links
[LinkedIn](https://www.linkedin.com/in/danhyunkim/)

[Github](https://github.com/danhyunkim)

[Blog](https://medium.com/@danhyunkim)

[Email](danhyunkim@gmail.com)

[Billboard 2018 Year-end Top 100](https://www.billboard.com/charts/year-end/2018/hot-100-songs) | 
[Billboard 2013 Year-end Top 100](https://www.billboard.com/charts/year-end/2013/hot-100-songs) | 
[Billboard 2008 Year-end Top 100](https://www.billboard.com/charts/year-end/2008/hot-100-songs)

[Songfacts - 2018 songs](https://www.songfacts.com/browse/years/2018) | 
[Songfacts - 2013 songs](https://www.songfacts.com/browse/years/2013) | 
[Songfacts - 2008 songs](https://www.songfacts.com/browse/years/2008) 