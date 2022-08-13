# Bancho service

This service is likely the one which will change the least. The principal is fairly limited in terms of being able to split it up because of how osu!stable's protocol works. The most difference will be the stateless architecture, as a bancho service is usually the most stateful service by nature.

There are some key principles which will be different though.

## Events system

The bancho service should be extendible, and so most player interactions with the service should be relayable elsewhere. This event system should be implemented using something like a websocket where authorized users can listen to certain events on players and process it's data.

## External bot

Rather than having a bot hardcoded into the service in a rather cursed way, the bot will be an external project which will utilise the events system to operate. People can also create their own bots very easily in this fashion.

## Tournament support

No server has good tournament client (and IRC) support, and the new infrastructure should have good support - being able to deliver high-quality tournaments to the player base is a very important part of growing the community!

## No interruptions

As sessions will be stateless, server interruptions won't effect things like multiplayer - this is something that I think is incredibly important, as it's never nice to have your game interrupted by a server restart