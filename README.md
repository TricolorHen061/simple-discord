
<head>
  <meta charset="utf-8">
</head>
<body>
  <h1>Introduction</h1>
  <hr>
  <p>Simple Discord is a simple way to to make Discord bots in Python. This library is still in beta, so I recommend not using this in production yet.</p>
  <h1>How to Install</h1>
  <hr>
  <p>To install Simple Discord, you have to have Python pip3 installed on your machine. Run the following command in a Command Prompt or Terminal:</p>
  pip3 install simple-discord
  <p>And to update:</p>
  pip3 install -U simple-discord
  <h1>A Basic Bot</h1>
  <hr>
  <p>To keep things simple and easy to use, Simple Discord revolves around the use of parameters. A parameter is something you put in a function's parenthesis that tells the function how to behave. Lets look at an example:</p>
  <br>
  <code>
    
    from simple_discord import simple_discord #Import the library

    discord_bot = simple_discord.simple_discord_bot()

    discord_bot.add_command("!test", "You just created a Discord bot!") #The first two parameters are required. The first one is the message that you send to trigger the response, and the second one is the message the bot will respond with.
 
    discord_bot.add_command("!ping", "Pong!") #You have no limit on the commands you can add to your bot.
  
    discord_bot.set_token("Put your bot's token here") #Put your bot's token in the double quotes.
    
  </code>

  <br>
  <h3><b>CAUTION</b></h3>
  <p>The "set_token" method has to always come at the end of the file. This is because the "set_token" method will start your bot, and everything after that line will be ignored.</p>
  <h1>Adding Features to our Bot</h1>
  <hr>
  <p>In the last section, we created a bot that can only respond to command. Lets add some extra functionality to our bot. Here are all the parameters that simple_discord currently supports:</p>
  <b>reaction:</b> Needs the emoji itself copied and pasted into a string. A good website where you can get emojis from is <a href="https://getemoji.com/">getemojis.com</a>. The paramerter "react_to" is also needed for this to work.
  <br>
  <i>Type:</i> string
  <br>
  <br>
  <br>
  <b>react_to:</b> Bot will react to either the command that triggered the response, or the bot's response. Type "command" for the bot to react to the message that triggered the bot's reponse, or "response" for the bot to react to the bot's own response.
  <br>
  <i>Type:</i> string
  <br>
  <br>
  <br>
  <b>Delete:</b> If set to True, bot will delete the message that triggered the bot's response.
  <br>
  <i>Type:</i> boolean
  <br>
  <br>
  <br>
  <b>connect_to_voicechannel:</b> If set to True, bot will join the author's channel they are in. If they are not in one, bot will print an error to the console.
  <br>
  <i>Type:</i> boolean
  <br>
  <br>
  <br>
  <b>source_to_play:</b> Plays a source. Put the path/file name that you want the bot to play. Please note that the "connect_to_voicechannel" parameter must be set to True for this to work.
  <br>
  <i>Type:</i> boolean
  <br>
  <br>
  <br>
  <b>DM:</b> DMs the person that triggered the response a message.
  <br>
  <i>Type:</i> string
  <h1>Examples</h1>
  <hr>
  <p>Now that we have learned all the parameters the this library currently supports, we can do more advanced things with our bot. Lets look at some examples.</p>
  <br>
  Example of a bot that reacts with a 😁 to the person's message and DMs the person a message saying "Thank you for using this bot!":
  <br>
  <br>
  <code>
  
    from simple_discord import simple_discord #Import the library
    
    discord_bot = simple_discord.simple_discord_bot() #Make our object to connect to Discord.
    
    discord_bot.add_command("!hi", "Done.", react_to="command", reaction="😁", DM="Thank you for using this bot!")
    
    discord_bot.set_token("Put your bot's token here") #Put your bot's token in the double quotes.
  </code>
  <br>
  <br>
  Example of a bot that joins a voice channel and plays music from a file called "audiosource.mp3":
  <br>
  <br>
  <code>from simple_discord import simple_discord #Import the library
  <br>
  discord_bot = simple_discord.simple_discord_bot() #Make our object to connect to Discord.
  <br>
  discord_bot.add_command("!play", "Playing.", connect_to_voicechannel=True, source_to_play="audiosource.mp3")
  <br>
  discord_bot.set_token("Put your bot's token here") #Put your bot's token in the double quotes.
  </code>
<h1>Bot settings</h1>
<hr>
<p>You can set settings for your bot with the ".config" method. Here are the parameters/settings you can choose from:</p>

<b>show_dms:</b> If set to True, bot will print DMs it gets from people.
<br>
<i>Type:</i> boolean
<br>
<br>
<br>
<b>status:</b> Changes the status of the bot. Must be one of the following: "online", "idle", "do not disturb", and "offline".
<br>
<i>Type:</i> string
<br>
<br>
<br>
<b>activity:</b> Changes the bot's activity.
<br>
<i>Type:</i> string
<br>
<br>
<br>
<b>respond_to_other_bots:</b> If set to False, bot will not respond to other bots.
<br>
<i>Type:</i> boolean
<h1>Examples</h1>
<hr>
<p>Lets look at examples of how to use settings for your bot:</p>
<code>
  from simple_discord import simple_discord_bot #Import the library
  <br>
  discord_bot = simple_discord.simple_discord_bot()
  <br>
  discord_bot.add_command("!hi", "Hello!) #Add a command
  <br>
  discord_bot.config(show_dms=True, status="idle", activity="This is a bot made with simple_discord!") #Changing some settings
  <br>
  discord_bot.set_token("Token Here") #Put your token there.
</code>

<h1>Help and Support</h1>
<p>Join our <a href="https://discord.gg/ewf9WMJ">server</a> for help or comments about this library.</p>
</body>
