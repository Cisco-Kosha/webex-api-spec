# Kosha Webex Messaging Connector

Primarily known for its video conferencing capabilities, the Webex platform also includes a powerful messaging application. 

The Kosha Webex Messaging connector enables you to perform REST API operations from the Webex Messaging API in your Kosha workflow or custom application. Using the Kosha Webex Messaging connector, you can directly access the Webex platform to:

* Create a Webex space and invite people
* Search for people in your company
* Post messages in a Webex space
* Get Webex space history or be notified in real-time when new messages are posted by others
* Execute a command on a Webex RoomOS device

## Useful Actions 

You can use the Kosha Webex Messaging connector to manage messages, rooms, teams, and people.  

Refer to the Kosha Webex connector [API specification](openapi.json) for details.

### Messages

 In Webex, messages are sent directly between users or between multiple users in rooms. Use the messages API to send messages.

### Rooms

Rooms are virtual meeting spaces where people post messages and collaborate on work. Use the Rooms API to create and delete rooms and update rooms to change their titles or make them public.

### Teams

Teams are groups of people with a set of rooms that are visible to all members of that team. Use the Teams API to create and delete teams and update teams to change their names.

### People

People are registered users of Webex. Use the People API to list, create, update, and delete users.

## Authentication

To authenticate when provisioning the Kosha Webex connector, you need your [personal access token](https://developer.webex.com/docs/getting-started#/docs/getting-started#personal-access-token).
