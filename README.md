# music_sensibility
To detect music taste profile of Spotify users and provide recommendations . 
This application has access to a database of different kinds of music with attributes such as dancebility, energy, decade it belongs to, artist, acoustics, instrumentalness, popularity etc . This data is clustered. 
Given the user's favorite song, this aplication will locate the song in the cluster, then compare other songs closer to the favorite song located and recommend a playlist based on filters such as danceability & energy levels.


## User Flow 
The user picks their favorite song from the dropdown. The tolerance filter is set to 0.001, meaning the songs recommended are within this range of distance to the favorite song.  
Then the application runs the code to search & recommend the playlist by filtering further using the danceability & nergy filters. 

##Please see the screenshot attached to the repo


--Implementation logic 
1. Cleanse the data retrieved from spotify that is stord as csv
2. Use elbow method to identify optimum clusters 
3. Use PCA technique, Perform Kmeans clustering . Per data collcted, the optimal clusters were 3.
4. Request the user to enter their favorite song from a sample of 30 listed in the drop down 
5. Locate the favorite song in the clusters 
6. Calculate the  distance from the centeriod for all nodes 
7. Filter nodes closest to the favorite song located 
8. Set distance Tolerance as 0.001 and filter to identify nodes/points/tracks closest to the favorite song.
9. Filter by dancebility bandwidth 
10. Filter by Energy bandwidth 
11. Display playlist recommendation by sending a sample froom the filtered list. 

-- Instructions to run
streamlit run music_sensibility.py 

