ZipfSong
========

Spotify programming puzzle
http://www.spotify.com/se/jobs/tech/zipfsong/

Zipf’s Law is an empirical law originally formulated about word frequencies in natural languages, but it has been observed that many natural phenomena, such as population sizes and incomes, approximately follow the same law. It predicts that the relative frequency of the i’th most common object (in this case, a song) should be proportional to 1/i.

To illustrate this in our setting, suppose we have an album where all songs are equally good. Then by Zipf’s Law, you expect that the first song is listened to twice as often as the second song, and more generally that the first song is listened to i times as often as the i’th song. When some songs are better than others, those will be listened to more often than predicted by Zipf’s Law,  and those are the songs your program should select as the good songs. Specifically, suppose that song i has been played fi times but that Zipf’s Law predicts that it would have been	played zi times. Then you define the quality of song i to be qi = fi / zi. Your software should select the songs with the highest values of qi.

Input
The first line of input contains two integers n and m (1 ≤ n ≤ 50000, 1 ≤ m ≤ n), the number of songs on the album, and the number of songs to select. Then follow n lines. The i’th of these lines contains an integer fi and string si, where 0 ≤ fi ≤ 1012 is the number of times the i’th song was listened to, and si is the name of the song. Each song name is at most 30 characters long and consists only of the characters ‘a’-‘z’, ‘0’-‘9’, and underscore (‘_’).

Output
Output a list of the m songs with the highest quality qi, in decreasing order of quality. If two songs have the same quality, give precedence to the one appearing first on the album (presumably there was a reason for the producers to put that song before the other).

Sample input 1
4 2
30 one
30 two
15 three
25 four

Sample output 1
four
two

---

Sample input 2
15 3
197812 re_hash
78906 5_4
189518 tomorrow_comes_today
39453 new_genious
210492 clint_eastwood
26302 man_research
22544 punk
19727 sound_check
17535 double_bass
18782 rock_the_house
198189 19_2000
13151 latin_simone
12139 starshine
11272 slow_country
10521 m1_a1

Sample output 2
19_2000
clint_eastwood
tomorrow_comes_today
