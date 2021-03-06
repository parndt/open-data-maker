

# Open Data Maker
[![Build Status](https://travis-ci.org/18F/open-data-maker.svg?branch=master)](https://travis-ci.org/18F/open-data-maker)

The goal of this project is to make it easy to turn a lot of potentially large
csv files into open data via an API and the ability for people to download
smaller csv files with a subset of the data.

Preliminary research suggests that open data users (journalists and others)
actually know how to work with spreadsheets really well, but a lot of the
data sets that we have in government are huge.

The first version of this project will allow us to host a website for an
agency with a specific set of csv files, which are deployed with the app.
This will allows us to deploy more quickly since there will be a lower risk
security profile than if ab agency could upload the CSV files (which might
be a nice longer term feature).


## How this works

1. Make sure elasticsearch is running
1. Put csv files into /data
1. Import files from /data: ```rake import```

## TO DO

1. Import...
  1. there can be multiple files (must end in .csv)
  1. optional .yaml file that specified column -> field mapping
1. api endpoint to get the data
1. support multiple endpoints
