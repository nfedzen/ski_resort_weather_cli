# Pow Weather
> Your best ski resort weather report!

## Table of contents
* [General info](#general-info)
* [Intro Video](#intro-video)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)

## General info
Pow Weather is a CLI application for checking the weather and pow for your favorite Colorado Ski Resorts! Get up-to-date weather information for 22 ski resorts in CO
so you and your friends can get shreddy with that fresh butter.

## Intro Video
[Pow Weather on YouTube](https://youtu.be/9y9g1tRn49Y)

## Technologies
* Ruby 
* ActiveRecord - version 6.0
* Sinatra - version 2.0
* Sinatra-activerecord - version 2.0
* SQLite3 - version 1.4
* TTY-Prompt
* TTY-Spinner
* TTY-Box
* Rest-Client


## Setup
Get ready, to get shreddy. Run this app by cloning the repository from GitHub and running the following commands:
```ruby
bundle install
```
```ruby
ruby runner.rb
```

## Code Examples
```ruby
def forecast days, weather
    clear
    banner
    puts "The #{days} day weather forecast for #{@resort_name} is:"
    puts "\n"
    weather["daily"][1..days].each do |day|

      puts "Day: #{dateTime("#{day["dt"]}")} 🗓"
      puts "Temperature: #{day["temp"]["day"]}\xC2\xB0 F "    
      puts "Low: #{day["temp"]["min"]}\xC2\xB0 F 🔽" 
      puts "High: #{day["temp"]["max"]}\xC2\xB0 F 🔼"

      puts "Conditions: #{day["weather"][0]["main"]}"
      if day["weather"][0]["main"] == "Snow"
        puts "Amount of Fresh Pow: #{day["snow"]} in 🌨"
      end
      puts "Wind Speed: #{day["wind_speed"]} mph 💨"
      puts "\n"
    end
    pause
    welcome
  end
```



## Features
* Create a username and password 
* Select and save your favorite resorts
* Receive accurate weather forcasts for any Colorado ski resort
* Receive current weather, along with hourly, 3 day, 5 day, and 7 day forecasts


## Status
Project is: finished with potential for future features.


