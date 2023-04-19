# Kosha Webex Messaging Connector

![Webex](images/webex.png)

Primarily known for its video conferencing capabilities, the Webex platform also includes a powerful messaging application. 

Using the Kosha Webex Messaging connector, you can perform REST API operations to create, update, and delete messages. Using the Webex Messaging API, your Kosha workflow or application can directly access the Webex platform to:

* Create a Webex space and invite people
* Search for people in your company
* Post messages in a Webex space
* Get Webex space history or be notified in real-time when new messages are posted by others
* Execute a command on a Webex RoomOS device

## Useful Actions 

You can use the Kosha Webex Messaging connector to manage messages, rooms, teams, and people.  

Refer to the Kosha Webex connector [API specification](openapi.json) for details.

### Messages

 In Webex, messages are sent directly between users or between multiple users in rooms. Webex displays each message on its own line along with a timestamp and sender information. You can send messages formatted in plain text or Markdown, and send file attachments along with your messages.

You must be a member of a space to target it with the Messaging API.

### Rooms

Rooms are virtual meeting spaces where people post messages and collaborate on work. Use the Rooms API to create and delete rooms and update rooms to change their titles or make them public.

### Teams

Teams are groups of people with a set of rooms that are visible to all members of that team. Use the Teams API to create and delete teams and update teams to change their names.

### People

People are registered users of Webex. Use the People API to list, create, update, and delete users.

## Example Usage

The following request creates a message in a room: 

```
curl --request POST \
  --header "Authorization: Bearer ACCESS_TOKEN" \
  --url https://webexapis.com/v1/messages
{
  "roomId": "Y2lzY29zcGFyazovL3VzL1JPT00vYmJjZWIxYWQtNDNmMS0zYjU4LTkxNDctZjE0YmIwYzRkMTU0",
  "parentId": "Y2lzY29zcGFyazovL3VzL01FU1NBR0UvZWM1ZTIzZjAtN2RhMS0xMWU5LTg2NTgtZTkzYzNiODZjZmFm",
  "toPersonId": "Y2lzY29zcGFyazovL3VzL1BFT1BMRS9mMDZkNzFhNS0wODMzLTRmYTUtYTcyYS1jYzg5YjI1ZWVlMmX",
  "toPersonEmail": "julie@example.com",
  "text": "PROJECT UPDATE - A new project plan has been published on Box: http://box.com/s/lf5vj. The PM for this project is Mike C. and the Engineering Manager is Jane W.",
  "markdown": "**PROJECT UPDATE** A new project plan has been published [on Box](http://box.com/s/lf5vj). The PM for this project is <@personEmail:mike@example.com> and the Engineering Manager is <@personEmail:jane@example.com>.",
  "files": [
    "http://www.example.com/images/media.png"
  ],
}
```

## Authentication

To use the Webex REST API, you need a Webex account. The Kosha Webex Messaging connector uses `API_KEY` based auth using your [personal access token](https://developer.webex.com/docs/getting-started#/docs/getting-started#personal-access-token).
