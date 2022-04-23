
# VRChat Photon API Docs

This repo is a collection of things I and other Dev's close to me have documented over the years.

It will be updated on my freetime and will have it's own swagger.io page eventually

Currently only a list of events will be provided until I free up time with my other projects

# Documentation
## Events
Events are described by using an event code which are described by a byte value (0-255), and their context can be anything that PUN can serialize.


| Event Code      | Description |
| ----------- | ----------- |
| 1. Uspeak      | Used for sending voice data,  takes an array of bytes as it's datatype       |
|2. Executive Messages  |  System plugin messages
|6. VRCEvent|Used for sending Remote Procedure Calls (RPC) datatype is an array of bytes|
|8. Interest Management/Update Quality|
|7. Serialization/Unreliable|Object and Movement Sync takes an array of bytes |
|9. SDK3 Avatar Syncronization
|33. Player Moderations|Takes a <byte, Object> dictionary and is targeted|
|60. PhysBones |
|200. SendSerialize|
|202. PUN Object Instantiation|
|203. Terminate PUN Connection|
|204. Destroy PUN Object |
|205. Clear RPC Cache|
|206. SendSerializeReliable|
|208. Assign Master|
|209. Request Ownership Transfer|
|210. Ownership Transfer|
|223. AuthenticationValues|
|226. Join Room|
|230. PUN Authentication|
|252. Set Properties|
|253. Update Properties|



## RPC

Nothing to see here yet :)

## OperationCodes
Nothing to see here yet :)

## Example Code / Code Snippits
Nothing to see here yet :)



        



## Contributing

Contributions are always welcome!


Please follow basic common sense principles and remain respectful.

