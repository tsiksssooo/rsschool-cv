# Alexander Tsiklauri
## Contact Details:
* Email: a.tsiklauri@gmail.com
* Mobile: +351 966 672 604
* Based in: Cascais, Portugal

![profile picture](./atProfilePic.jpg)

## Profile:
I am a qualified full-stack web-developer with over a year of experience. Before turning to the tech industry, I worked as an investment analyst / manager, mostly dealing with real estate projects around the world. Always ready to learn and work in a team. Love surfing.

## Skills:
* HTML
* CSS
* JavaScript
* React
* ESJ
* Git
* MongoDB
* Node.js

## Education:
* **March 2022 - March 2023**
    Rolling Scopes School - JS / FRONT-END COURSE

* **2005 - 2011**
    Higher School of Economics / ESCP Paris

## Experience:
* **2012 - 2021**
    Investment Analyst / Manager

## Languages:
    English - C1 / C2
    Portuguese - B1 / B2
    Spanish - B1
    Russian - Native Speaker

## Code Example:

```
  function apiCall(coord1, coord2, response) {

        const now = Math.floor((new Date()) / 1000) + 3600;
        const end = now + 3600;
        const lat = coord1;
        const lng = coord2;
        const params = 'swellHeight,swellPeriod,airTemperature,cloudCover,swellPeriod,visibility,windDirection,windSpeed,waterTemperature';

        fetch(`https://api.stormglass.io/v2/weather/point?lat=${lat}&lng=${lng}&params=${params}&start=${now}&end=${end}`, {
            headers: {
                'Authorization': apiKey
            }
        }).then((response) => response.json()).then((jsonData) => {
            console.log(jsonData.meta);
            let swellSize = jsonData.hours[0].swellHeight.sg;
            let swellPeriod = jsonData.hours[0].swellPeriod.sg;
            let waterTemperature = jsonData.hours[0].waterTemperature.sg;
            let airTemperature = jsonData.hours[0].airTemperature.sg;
            let windSpeed = jsonData.hours[0].windSpeed.sg;
            let windDirection = jsonData.hours[0].windDirection.sg;
            let cloudCover = jsonData.hours[0].cloudCover.sg;

            if (swellSize > 1) {
                res.render('waves', {
                    message: "YEAAAAAAAAAAAH MAN!",
                    swellH: swellSize,
                    swellP: swellPeriod,
                    waterT: waterTemperature,
                    airT: airTemperature,
                    windS: windSpeed,
                    windD: windDirection,
                    cloudC: cloudCover,
                    message2: "GO HAVE SOME FUN!",
                });
            } else {
                res.render('waves', {
                    message: "SORRY BRO, NO WAVES OUT THERE :(",
                    swellH: swellSize,
                    swellP: swellPeriod,
                    waterT: waterTemperature,
                    airT: airTemperature,
                    windS: windSpeed,
                    windD: windDirection,
                    cloudC: cloudCover,
                    message2: "GO FOR A BIKE RIDE INSTEAD!",
                });
            };
        });
    };
```


