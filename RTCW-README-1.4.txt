   Return To Castle Wolfenstein -- version 1.4
NOTE to server administrators and mod developers
    =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=

There is a number of changes in version 1.4 of 
Return To Castle Wolfenstein which are particularly 
relevant to server administrators and mod 
developers. This note highlights the new features
of multiplayer servers.

New vote flags configuration
----------------------------

The Multiplayer Server Creation menu provides a 
simple interface to configure which votes are 
allowed on the server, and which are not. If you 
don't use the graphical user interface, you can
configure the votes in game with the g_voteFlags 
cvar. g_voteFlags 0 will disable voting completely
and g_voteFlags 255 will allow all votes. For a
more precise configuration, see the list below:

Restart Map    1
Reset Match    2
Start Match    4
Next Map       8
Swap Teams    16
Game Type     32
Kick Player   64
Change Map   128

Add up the values of the votes to be allowed and
set g_voteFlags accordingly.

Server URL and mod URL
----------------------

The in-game server browser has a server information
button which can display URL and mod URL buttons. 
These buttons will close the game and open the web browser
to URLs configured by the server. There are two cvars
to configure the URL buttons:

URL is a serverinfo cvar that the server administrator
should set to point to a web page about his server.
Game statistics, players forum, etc.

mod_URL can only be set from the mod code. Mod 
developers should set mod_URL to point players to the
official web pages of their mod. This will spread
the news about your mod and get new players involved
faster.

Please note that URL cvars are configured as serverinfo.
Third party game browsers will be able to support these
features as well.

