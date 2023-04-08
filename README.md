# Kosha Webex Messaging Connector

Webex is known for its video conferencing and screen sharing, but messaging is a core element of the platform due to the relaxed and straightforward nature of the medium. Messages are conversational, fluid, and natural without requiring the participants of the chat to be engaged at that very moment. Participants can review and respond to chats when its convenient to their needs and circumstances.

The Messaging API is an easy-to-use Restful platform that allows you to create, update, and delete messages. Every message is tagged with sender information (who wrote the message) and the local timestamp (what time did they sent it relative to you). Alternatively, you can change the format of the messages sent (between plain text or markdown) or send a file attachment along with your message to the chat room.

## What is possible with Webex APIs?

The Webex APIs provide your applications with direct access to the Cisco Webex Platform, giving you the ability to:

* Create a Webex space and invite people
* Search for people in your company
* Post messages in a Webex space
* Get Webex space history or be notified in real-time when new messages are posted by others
* Execute a command on a Webex RoomOS device
and much more!


The Webex APIs are RESTful. In REST, each resource is represented by a base URL like /messages and the HTTP methods GET, POST, PUT and DELETE are used to request data and perform actions on those resources.

For methods that accept request parameters the platform accepts either `application/json` or `application/x-www-form-urlencoded` content types and currently only supports returning data in `application/json` format.


## Useful Actions 

### Messages

Messages are how you communicate in a room. In Webex, each message is displayed on its own line along with a timestamp and sender information. Use this API to list, create, update, and delete messages.

Message can contain plain text, rich text, and a file attachment.

Just like in the Webex app, you must be a member of the room in order to target it with this API.

### Rooms

Rooms are virtual meeting places where people post messages and collaborate to get work done. This API is used to manage the rooms themselves. Rooms are created and deleted with this API. You can also update a room to change its title or make it public, for example.

To create a team room, specify the a teamId in the POST payload. Note that once a room is added to a team, it cannot be moved.

### Teams

Teams are groups of people with a set of rooms that are visible to all members of that team. This API is used to manage the teams themselves. Teams are created and deleted with this API. You can also update a team to change its name, for example.

### People

People are registered users of Webex. Searching and viewing People requires an auth token with a scope of spark:people_read. Viewing the list of all People in your Organization requires an administrator auth token with spark-admin:people_read scope. Adding, updating, and removing People requires an administrator auth token with the spark-admin:people_write and spark-admin:people_read scope.

Refer to the Webex connector [API specification](openapi.json) for details.

## Example Usage

< sdk example? >

## Authentication

To use the Webex REST API, you'll need a Webex account. The connector uses API_KEY based auth using your personal access token.

 In REST, each command is represented by a base URL like /messages and the HTTP methods GET, POST, PUT and DELETE are used to perform tasks such as request data or perform actions on those resources such as configure your device, start video calls from code, create custom In-Room Controls, and deploy Macros on your devices.