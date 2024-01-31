This is a ruby fork of the buildpack.

# MaxMind Build Pack
Ensure your application has the latest copy of MaxMind data when deploying. 

## How it Works
The database file(s) is saved to a Heroku cache directory that is persisted across builds. 
- If the database file does not exist, a new copy is downloaded.
- If a new file exists on MaxMind server, it is downloaded.

## Required Environment Variables
* MAXMIND_KEY = The license key they provided which allows you to download files.
* MAXMIND_EDITIONS = Comma delimited list of databases to download ie: "GeoIP2-ISP,GeoIP2-City,GeoIP2-Country"
