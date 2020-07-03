title	date	tags	header	excerpt	toc_label	toc_icon
#Then I come through with my ABC: Grime Scene Analysis
2020-06-20
topic-model
lyrics
rap
image:"../assets/images/halong_bay.jpg"
Understanding the words behind the UK Rap scene
UK Rap Analysis
microphone
UK rap music prides itself on lyricism; wordplay, themes, and multitiered rhyme schemes. These components of a rap song are just as important as the beat. There is much emphasis on what is being said; it could be an insult, reference to pop culture or a callback to someone in the rap-scene. This focus on words is a big part of grime and the best lyrics can earn an artist a wheel-up (or 3).

As a result, I thought it would be interesting to have a look at the words behind the UK Rap scene. This post won't contain any code snippets (happy to share if anyone is interested). First we will look at some descriptive statistics relating to the contribution of each artist to the scene, before doing some natural language processing activities.

whatusayin

The Data Set
Genius is a go-to for lyrics and understanding the multiple meanings of some lines. They kindly provide an API through which to access this wealth of information. Using the API we can pull lyrics from any given artist. I created a list of UK rappers and queried the API, this process took a long time as not to overload the server with requests. I understand there may be some artists missing, so please let me know if you'd like to see anyone else in there! The data used contains all lyrics on LyricGenius related to the selected artists shown in the pie chart below. Contains 4742 songs from 45 artists containing 2,220,363 words.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~ysohoye1/8.embed" height="525" width="100%"></iframe>
The interactive chart shows contribution of songs by each rapper to this data set. Immediately we can see how productive Wiley has been, over 100 more songs than Ghetts. Other leading contributors include the old guard of Giggs, Kano and the once new kid on the block: Chip. M.I.A. is another veteran of the scene and contributes a similar amount to Skepta, Dizzee Rascal and JME. Bugzy Malone and Little Simz have the biggest contribution of the newer rap artists. By no means is this the definitive list of UK Rap contributions, this list is obtained from lyric genius and although it does a good job of posting freestyles and mixtapes - there will be some lyrics not posted.

headiewalk

Lyrics for Lyrics
Since song contributions looks more like a timeline of the rap scene, maybe a look at the words within the songs may help. The chart below looks at unique words; showing the average number of unique words per song on the y axis and the average number of words per song on the x. Moving up towards the top of the chart shows more unique words used in a song. Whereas moving rightward shows there are more words in a song. Size of the bubbles indicates the number of songs, this provides a good indication of sample size e.g. Mike Skinners solo effort only contains 1 song whereas The Streets have 119.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~ysohoye1/11.embed" height="525" width="100%"></iframe>
The trend is expected: as you say more words in a song you are bound to use more different words, therefore move to the top right of the graph. Two artists on the top right (Mic Righteous and [Dave](https://www.youtube.com/watch?v=XFko_Xf-H30) ) are packing a lot of different words into their songs. This could be used as a measure of lyricism, they are 2 artists certainly knows for their lyrics. Not too far behind them are a selection of known wordsmiths: Cadet, Bugzy Malone, P Money, Lowkey, and Akala. Towards the bottom left of the chart we have the less wordy rappers, MIA and MIST have 126 and 142 unique words per song on average.
Where do you know me from?
Representing your city or area is an element of rap culture. Especially as the scene expands further out of London; area codes make good ad-libs. Geo-encoding is the method of extracting place names out of text. Using all lyrics in the data set, place names have been extracted. London is by far the most talked about place in the grime scene. In fairness, it has had a head start advantage as in the early days a lot of the scene was based in London therefore lot's of rappers were talking about London, so much so that even East London makes the top 5. There is also references to Meridian Estate in Tottenham, where a lot of the original grime MCs were from. Nice is picked up a lot in the lyrics, but I don't think artists were referring to the area in France. A good example of the shortfalls of working with language and textual data, and why context is important.

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plot.ly/~ysohoye1/32.embed" height="525" width="100%"></iframe>
# What you saying?
A large part of working with language dat is the cleaning of it; data must be cleaned, removing stop words and making sure all words are lower case. In this particular instance, it also meant censoring expletives, of which there were many different kinds.After this we can produce a word cloud, this is an image showing the most popular words in UK Rap lyrics, the size indicates the frequency of that word.
