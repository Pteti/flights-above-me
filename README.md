# flights-above-me
Displays a flight directly above you in a fancy display.

Inspired by https://github.com/smartbutnot/flightportal but uses just Javascript + Browser. Uses flightradar24 free API + corsproxy.io.

Has basic PWA support for iOS, so if you open this on an iPad, you can tab Add to Home Screen and it will become a fancy display.

<img width="1498" alt="image" src="https://github.com/user-attachments/assets/530403ef-e8b5-4223-b4aa-0241255c933e" />

# CORS Proxy

Because flightradar24 has CORS headers you need a CORS proxy. This uses https://corsproxy.io which works well. If you go over their limits, you can sign up for their paid version for $3/mo and pass ?corskey=<apikey> to index.html

# Location

By default this shows flights above London. Go to https://bboxfinder.com if you want to find your own box. Remember that the format bbox uses is a bit different. In the coordinates format choose Lat/Long and then flip them further. For example:

If the coordinates from bbox finder are:

```
Box 35.317366,-81.035156,42.423457,-65.039063
```

Flip first and third, to:
```
35.317366,42.423457,-81.035156,-65.039063
```

Use this location in `index.html?bounds=<location>`
