# Starter bots
Entelect will provide starter bots for the following languages:

* .Net Core (C#)
* Python 
* Javascript
* Java

Starter bots are the bare essentials you need to get going with very little decision making capability. They are built to be able to read in game files and make a random move.

The reference bot on the other hand is capable of playing a game from start to finish with some cleverness built in. This is there to help contestants who want something a bit smarter to work from.

## Additional languages

For any additional languages (except C#, Java, Javascript and Python 3) we will be relying on the community to contribute. 

To submit a new language for the tournament the following will need to be provided :

1. Starter Bot for that language
	* These will follow the same basic rules that all other starter bots use (listed below).
2. A Readme file detailing:
	* All prerequisites and requirements for the languages, detailed with versions, required for building and running the language's environment. 
	    * Ensure these are installed in the container.
	* CLI commands and procedure for compiling the project (ideally into an executable).
	* Instructions to ensure the bot can be exported with the required packages it needs to be executed.
        * Example, in the case of Java, ensuring the jar file is compiled with dependencies.
        * This is necessary due to the bots not running in the same environment they are compiled in.
	* CLI commands to run the bot, which will be used to run all bots supplied for this language.
	* Any relevant reference material that would help others who want to use this language.
3. A Docker container with environment for the language setup
	* Details on how to create the docker container will be added shortly.

Submissions for additional languages will close on **TBH**, after which no more starter bot or language requests will be accepted.

When submitting a new starter bot, a Pull Request to **this** repository needs to made. The Entelect Challenge team will then review the starter bot code as well as test the Docker container. Please ensure the `Dockerfile` is located in the **same** folder as the starter bot. In other words, the pull request will consist of the following files, in the **same** folder:
- Starter bot source code
- Readme file
- Dockerfile

## Starter bots submission rules

Before submitting a new starter bot you should make sure of the following:

1. Your bot has a `bot.json` file.
2. It is able to compile on any system, but most importantly in **Linux**.
3. Should not produce any errors when executing.
4. Should have a valid `Docker image` that can compile and execute any bot written in that language.

The bot itself needs to follow some basic rules:

1. Read in the state.json (or map.txt) and parse it into a easy to use structure
	* Details like the commands, car, powerups, map size, etc should be read from the state file. It should **NOT** be hardcoded.
2. Otherwise choose a block in a random direction and do one of the following things
    * Accelerate, decelerate or change lane.
    

## Building the Docker Containers

This year all bots will run within their own docker containers. To faciliate this, the submission of a new language for the tournament will also require a docker container that will support the running and compiling of the language.
		
### More detailed information to follow shortly.

Once your starter bot and docker container has been created. Create a pull request on github with the starter bot as well as the relevant docker container.
If you require any assistance building the continers please feel free to contact us at challenge@entelect.co.za.