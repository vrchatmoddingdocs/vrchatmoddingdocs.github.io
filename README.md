
# VRChat Photon API Docs

API Docs for VRChats PUN API Config

This repo is a collection of things I and other Dev's close to me have documented over the years.

It will be updated on my freetime and will have it's own github.io page eventually

Currently only a list of events will be provided until I free up time with my other projects

# Documentation
## Events
Events are described by using an event code which are described by a byte value (0-255), and their context can be anything that PUN can serialize.

See https://doc.photonengine.com/en-us/pun/current/gameplay/rpcsandraiseevent#raiseevent for more info


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




## RPC

Nothing to see here yet :)

## OperationCodes

See: https://doc-api.photonengine.com/en/pun/v1/class_operation_code.html#details for more details

PUN uses these contants interally and should be universal between most games

| Event Code  | Name | Description |
| ----------- | ----------- | ----------- |
|223    | AuthenticationValues  |               |
|226    | Join Room             |               |
|230    | PUN Authentication    |               |
|252    | Set Properties        |               |
|253    | Update Properties     |               |

## Example Code / Code Snippits

[Click Here!](Code-Snippets/)



        
## Why am I getting banned?

VRChat for the most part only has one automated system for bans, and that is through photon, so please be careful when trying anything out, or use an alt account & a vpn.

These are some frequest causes for bans when interacting with photon on VRChat, please double check everything is correct before you attempt anything in-game.

- You are sending an incorrect datatype
- EventOptions paramaters are invalid
- You are surpassing a ratelimit
- You are sending impossible data (EX: Null data through Uspeak/Event 1)


## Contributing

Contributions are always welcome!

If you would like to be a collaborator please message me on discord! tope#0001

Please follow basic common sense principles and remain respectful.

