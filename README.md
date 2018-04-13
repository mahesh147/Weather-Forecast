# Weather-Forecast

## What is this repo about?

This repo contains the source code for a web app that displays the weather forecast for any city.

## What is the tech-stack?

This web-app was made with React. Redux was used for state management, and Redux-Promise was used as middleware. Axios was used to make API calls.

## Where is the weather forecast information collected from?

openweathermap.org has a really good API system in place. This web-app leverages from that.

## How do I run this locally on my machine?

 - Download or clone this repo.
 - Navigate to the project folder and run - npm install.
 - To set up the local dev server, run - npm start.
 - Open your browser and navigate to the specified localhost.

## Where is the API_KEY?

My API_KEY has been excluded from this public repo. You'll need to use your own API_KEY if you want to run this locally. Go to http://openweathermap.org/api , you'll probably have to signup for an account before you get an API key.

Once you have the API_KEY, add the following line of code to WeatherForecast/src/actions/index.js :

	const API_KEY = 'YOUR API_KEY GOES HERE'

## How do I fetch the weather forecast data for countries other than India?

By default, the web-app will only fetch weather forecast for places in India, if you want to change it then, edit the following line of code in WeatherForecast/src/actions/index.js :

	export function fetchWeather (city) {
                                                                       
		const url = `${ROOT_URL}&q=${city},[ENTER THE COUNTRY CODE THAT YOU WANT TO FETCH WEATHER FORECAST DATA FROM]`;

		...// Rest of the code

	}

For example, if you want to change the country to US, then:
	
		const url = `${ROOT_URL}&q=${city},us';

For Germany, that would be :
		
		const url = `${ROOT_URL}&q=${city},ge';

...so on and so forth.

### NOTE

If you like this project, consider giving it a star. I'd appreciate it. :D

