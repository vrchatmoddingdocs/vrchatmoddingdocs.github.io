---
title: Pun Docs
layout: template
filename: photon
--- 



# VRChat PUN Docs
 
Welcome to the VRChat Modding Docs!

This page will be  updated on my freetime with the help of other contributers and team members, you can expect documentation on Event Codes, Operation Codes, and even some basic Code Snippets!

If you would like to contribute please feel free to make a pull request on the github!

# Documentation

## Events

[Click Here for more Info!](https://doc.photonengine.com/en-us/pun/current/gameplay/rpcsandraiseevent#raiseevent)
Events are described by using an event code which are described by a byte value (0-255), and their context can be anything that PUN can serialize.

| Event Code | Human-Readable Name | Other Name | Description |
| ----------- | ----------- | ----------- | ----------- |
| 1 | Uspeak                            |                                   | Used for sending voice data,  takes an array of bytes as it's datatype       |
| 2 | Executive Messages                | Kick message                      | System plugin messages                                                       |
| 3 | Master Client Sync                |                                   |                                                                              |
| 4 | Cached Event                      |                                   |                                                                              |
| 5 | MasterClientSyncFinished          |                                   |                                                                              |
| 6 | VRCEvent                          |                                   | Used for sending Remote Procedure Calls (RPC) datatype is an array of bytes  |
| 8 | Interest Management/Update Quality|                                   |                                                                              |
| 7 | SerializationUnreliable           | FloatBufferNetworkSerializer      | Object and Movement Sync takes an array of bytes                             |
| 9 | SDK3 Avatar Syncronization        |                                   |                                                                              |
| 33 | Player Moderations               |                                   | Takes a <byte, Object> dictionary and is targeted                            |
| 35 | HeartBeat                        |                                   |                                                                              |
| 40 | Avatar Refresh                   |                                   |                                                                              |
| 60 | PhysBones                        |                                   |                                                                              |
| 69 | BestEvent                        |                                   |    Best Photon Event  |
| 200 | SendSerialize                   |                                   |                                                                              |
| 202 | PUN Object Instantiation        |                                   |                                                                              |
| 203 | Terminate PUN Connection        |                                   |                                                                              |
| 204 | Destroy PUN Object              |                                   |                                                                              |
| 205 | Clear RPC Cache                 |                                   |                                                                              |
| 206 | SendSerializeReliable           |                                   |                                                                              |
| 207 |  Destroy Player                 |                                   |                                                                              |
| 208 | Assign Master                   |                                   |                                                                              |
| 209 | Request Ownership Transfer      |                                   |                                                                              |
| 210 | Ownership Transfer              |                                   |                                                                              |                                                                 

## OperationCodes

[Click Here for more Info!](https://doc-api.photonengine.com/en/pun/v1/class_operation_code.html#details)
PUN uses these operation code constants interally and should be universal between most games

| Event Code  | Name | Description |
| ----------- | ----------- | ----------- |
|217    | GetGameList           | Get the game list matching a supplied sql filter (SqlListLobby only)                          | 
|218    | SetServerSettings     | Operation to set some server settings. Used with different parameters on various servers      |
|219    | WebRpc                | WebRPC Operation                                                                              |
|220    | GetRegions            | Get list of regional servers from a NameServer.                                               |
|221    | GetLobbyStats         | Request statistics about a specific list of lobbies (their user and game count).              |
|222    | FindFriends           | Request the rooms and online status for a list of friends (by name, which should be unique).  |
|223    | AuthenticationValues  |                                                                       |
|226    | JoinGame              | Join game (by name)                                                   |
|227    | CreateGame            | Creates a game (or fails if name exists)                              |
|228    | LeaveLobby            | Leaves lobby (on master)                                              |
|229    | JoinLobby             | Joins Lobby (on master)                                               |
|230    | Authenticate          | Authenticates this peer and connects to a virtual application         |
|231    | AuthenticateOnce      | Authenticates this peer and connects to a virtual application         |
|248    | ChangeGroups          | Operation code to change interest groups in Rooms (Lite application and extending ones). |
|250    | ExchangeKeysForEncryption|                                                                    |
|251    | GetProperties         | Get Properties                                                        |
|252    | SetProperties         | Set Properties                                                        |
|253    | UpdateProperties      | Update Properties                                                     |
|254    | Leave                 | Code for OpLeave, to get out of a Room                                |
|255 / ByteMaxValue   | Join                  | Code for OpJoin,  to get into a room.                                 |      

       
## Why am I getting banned?

VRChat for the most part only has one automated system for bans, and that is through photon, so please be careful when trying anything out, or use an alt account & a vpn.

These are some frequest causes for bans when interacting with photon on VRChat, please double check everything is correct before you attempt anything in-game.

- You are sending an incorrect datatype
- EventOptions paramaters are invalid
- You are surpassing a ratelimit
- You are sending impossible data (EX: Null data through Uspeak/Event 1)