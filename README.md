C2-Socket.io-dev
================

Applied some mods to the already modified Zack0Wack0's original. Taken from JohnnySheffields version.



###New Expressions:

Socket.DataAtVAr("variable name") <- this will allow you to select incoming values by using the variable name.

e.g. if the sever sent {id:5, x:2, y:5} for an event "move player", you can do On event "move player" > Opponent.X = int(Socket.DataAtVar("x"))

Socket.LoadDataJSONStringify <- this can be injected into a hash table or anything that takes a JSON string.

###New Action:

EmitAsJSONString <- this will allow you to send data as JSON. It will convert the JSON string to JSON prior to sending. Note, because C2 does not allow using escape characters like \ or the use of single quotes. You need to escape double quotes using "".

e.g: "{""y"":""" & int(MyPlayer.Y) & """}"

converts to {y:value}
