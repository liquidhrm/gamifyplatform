# Gamify Platform REST API

## Interface summary

## GamifyPlatform Web Admin Console 

GamifyPlatform Web Admin Console provides game registration for the game developers. During the registration process, an application ID and a service user is generated and binded to the game. The application ID is unique for each game and identified the game in the Gamify Platform. The service user provides access to game related management function.

## Endpoint types
The following REST endpoints are organized into two categories:

A) Administration endpoints provides user and/or game item management (accessible by using service user)

B) User related (in game) endpoints provides user interactions (accessible by the actualy logged in user/player).

## Login and authorization token
Successfull login is required, in order to interact with any of the following API call. At login, the game client should provide the authentication credentials by utilizing HTTP Basic authentication scheme. The login response contains the authorization token which is used later on.

## User types
There are two user types in the system:

A) service user, which is directly binded to a game

B) end user, who plays the game. The end users are registered to the Gamify Platform globally and belongs to one or more games.

## Security
After login, all subsequent endpoints are secured by Bearer authentication (also called token authentication). Therefore, each request must send the authorization token (received at login) in the 'Authorization' HTTP header as a 'Bearer' value.
