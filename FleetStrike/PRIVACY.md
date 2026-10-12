# Privacy Policy for Fleet Strike

**Effective date:** October 12, 2026

Fleet Strike ("the app") is published by Anirudh Maheswaram, an individual developer publishing under the name EastWest2032 ("we", "us"), who is the data controller for the information described here. This policy explains what information the app handles, why, and the choices you have. It applies to the Android app with the package name `com.eastwest2032.fleetstrike`.

## Summary

- No account, name, email address, or phone number is required to play.
- The app has no username, profile, or free-text chat.
- The app contains no advertising and no analytics SDKs.
- We do not sell your information or share it for advertising.
- Solo games are played entirely on your device, and no solo game data leaves it.
- Online multiplayer uses Google Firebase to connect two players and relay game messages.

## Information the app handles

### Solo mode

Solo games against the AI run entirely on your device and need no network connection. The app does not transmit any solo game data.

The app includes the Firebase software used for online multiplayer, and that software loads when the app starts. If you have played online before, it may contact Google to keep your anonymous sign-in valid, including while you play solo.

### Local multiplayer (Wi-Fi or hotspot)

Local games connect two devices directly over the same network, without any server.

- The hosting device broadcasts a discovery signal containing the room code to the local network, about once per second, until an opponent connects. Any device on that network can receive this signal.
- The joining device connects directly to the host, either by receiving that signal or by using a host address that you type in.
- Each device learns the other's local network address, as with any direct network connection.
- The two devices exchange the room code and the game messages described in the table below.

The app does not send any of this information to us or to any server.

### Online multiplayer (cloud rooms)

The first time you create or join an online room, the app signs you in anonymously with Firebase Authentication. The following information is then processed through Google Firebase:

| Information | Purpose |
|---|---|
| A random anonymous identifier, created by Firebase Authentication | To identify the two players in a room and to limit who can read and send its game messages |
| A six-digit room code, generated at random by the app for the host and typed in by the joining player | To match you with your opponent |
| Game messages: ready signals, shot coordinates, shot results (hit or miss, the type of any ship sunk, and whether the game is over), rematch requests, disconnect signals, and quick-chat phrases chosen from a fixed list in the app | To synchronize the game between the two devices |
| Times taken from your device's clock: when the room was created, when each message was sent, and a heartbeat sent about every 10 seconds | To detect disconnections and clean up abandoned rooms |
| IP address and technical connection details | Received automatically by Google when your device connects to Firebase, as described in Google's documentation linked below |

Your fleet layout is never sent. Your opponent learns only the result of each shot.

The app sends and displays only the fixed quick-chat phrases. Any other chat text it receives is discarded.

The app uses Firebase App Check with Google Play Integrity to confirm that requests come from a genuine copy of the app. This involves Google processing device and app integrity signals, and it is used only to protect the service against abuse.

The app does not link the anonymous identifier to your name, your Google account, your contacts, or any advertising identifier.

### Information the app does not collect

The app does not collect or access your name, email address, phone number, contacts, photos, files, microphone, camera, location, advertising ID, or payment information.

## Permissions

| Permission | Why it is declared |
|---|---|
| Internet | Online multiplayer and direct device-to-device connections |
| Network state | To check whether an internet connection is available, so the app can default to online or local play |
| Wi-Fi multicast | To discover another player's device on the same local network |

The app requests no other permissions.

## How information is used

Information is used only to run the game: to connect players, relay game messages, keep rooms in sync, remove inactive rooms, and protect the service against abuse. We do not use it for advertising, profiling, or marketing.

## Legal basis

Where data protection law requires a legal basis, we process the information above because it is necessary to provide the online game you asked for when you create or join a room. Keeping rooms limited to their players and removing inactive rooms is also in our legitimate interest in running a secure service.

## Sharing

We do not sell, rent, or trade your information.

Information is shared only in these cases:

- **Your opponent.** The other player in your room receives the game messages needed to play.
- **Other players with your room code.** The room record (room code, room status, the two players' anonymous identifiers, and heartbeat times) can be read by any signed-in user of the app who has the room code. Game messages can be read only by the two players in the room.
- **Google Firebase.** Google LLC processes online multiplayer data on our behalf as a service provider. Google's handling of this data is described in the [Firebase Privacy and Security documentation](https://firebase.google.com/support/privacy) and the [Google Privacy Policy](https://policies.google.com/privacy).
- **Legal requirements.** We may disclose information if required by law or a valid legal process.

## Retention and deletion

- **Rooms and game messages.** The app deletes an online room and its messages when either player leaves the room or exits the game, or when a player's device has had no contact from the opponent for more than 60 seconds. If the app is force-closed, loses its connection, or the deletion fails, the room can remain on the server. It is then removed when the same room code is created again, or when someone tries to join it after it has been inactive for more than 3 minutes. As a backstop, every room and every message carries an expiry time 24 hours after it was created, and Firebase deletes expired data automatically, typically within a further 24 hours.
- **Anonymous identifier.** The identifier is stored on your device and as a record in Firebase Authentication. That record is not deleted automatically. Clearing the app's data or uninstalling the app removes the identifier from your device, and a new one is created the next time you play online. The app turns off Android backup and device transfer for its data, so the identifier is not carried over to a reinstall or a new device.
- **Deletion requests.** Once you have played online, your identifier is shown as "Player ID" at the bottom of the app's lobby screen, where you can select and copy it. Send it to the address below and we will delete the matching Firebase Authentication record, and any room data linked to it, within 30 days. We hold nothing else that identifies you, so without the Player ID we cannot locate a specific record.

## Security

- Data sent to Firebase is encrypted in transit using TLS.
- Server-side security rules allow game messages to be read and sent only by the two players in a room, and prevent rooms from being listed or browsed. Rooms that are closed or abandoned can be deleted by any signed-in user of the app, which is how stale rooms get cleaned up.
- A room code is six digits and is not a password. Anyone using the app who has the code can read the room record and can join the room while it is waiting for an opponent.
- Data exchanged in local multiplayer travels directly between the two devices as unencrypted text, so play local games only on networks you trust.

No method of transmission or storage is completely secure, and we cannot guarantee absolute security.

## Children's privacy

The app is intended for players aged 13 and over and is not directed at children under 13. We do not knowingly collect personal information from children under 13. The app requires no account and asks for no personal details. If you believe a child under 13 has used the online mode, contact us at the address below with the Player ID and we will delete the associated record.

## International processing

Firebase is operated by Google, which may process data on servers located outside your country, including in the United States. For such transfers Google relies on the safeguards set out in its data processing terms, such as the EU–U.S. Data Privacy Framework and Standard Contractual Clauses, as described in its policies linked above.

## Your rights

Depending on where you live, you may have the right to access, correct, delete, or restrict the processing of your personal information, or to object to it, and to lodge a complaint with your local data protection authority. To exercise any of these rights, contact us at the address below. We will respond within 30 days. As explained under "Deletion requests", we need your Player ID to locate your record.

## Changes to this policy

We may update this policy as the app changes. Updates will be posted on this page with a new effective date.

## Contact

Questions or requests about this policy can be sent to: **eastwest2032@icloud.com**
