Bojack DOT Gif
-------------

This is a fork of the excellent [star wars dot gif project](https://github.com/LindseyB/starwars-dot-gif).

Without the work of [LindseyB](https://github.com/LindseyB), this version would not be possible!

First, I am a mad fan of [Bojack Horseman](http://www.imdb.com/title/tt3398228/).

I thought it would be awesome to have an animated gif with subtitles from the four seasons of the show.

You can follow [@BojackDotGif](https://twitter.com/BojackDotGif) on twitter.

I had to do some customizations of the original code as it focused on four Star Wars movies.

This version focuses on 48 episodes across 4 seasons. I will update the instructions here and do a blog
post on the customizations soon.

### To Use
Copy the contents of ```config.cfg.example``` into ```config.cfg``` and make sure to change the paths for VLC and the Star Wars episodes. Any format that can be read by VLC should be acceptable for the movies. Note, if you don't plan on running the twitter bot you only need to fill out the general section of the cfg file. 

To Run with search UI [(sample run)](http://www.youtube.com/watch?v=n387eBqnw1o):

Install requirements:

```
$ pip install -r requirements.txt
```

The gif is always created as **star_wars.gif**

```
$ python star_wars_gif.py
```


To get a random gif:

```
$ python makeGifs.py
```

If you want to use ```makeGifs``` elsewhere use:

```python
from makeGifs import makeGif
# source should be 4, 5, or 6
# index is the index of the SRT
makeGif(source, index)
```

Running the twitter bot:

- make sure you create API accounts for both twitter and imgur
- update **config.cfg*** to have the keys for both
- run ```$ python twitter_bot.py```

The bot will tweet once every 15 minutes.


**Note:** If generating gifs is taking too long for you remove ```nq=10``` from the ```writeGif``` call at the sacrifice of quality.
