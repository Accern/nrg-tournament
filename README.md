# Tournament App Requirements

## High Level Description

You are in charge of creating a bracket tournament manager web application. This app will manage the state of a tournament from beginning to end.

Here is more information on a bracket tournament in case you are unfamiliar: https://en.wikipedia.org/wiki/Bracket_(tournament)

The application should contain 16 participants that are matched up, and if you click on one of the participants that are matched up, then that participant will advance to the next round.

For example, given the following bracket:
```
_Adrian__

         \________

_Kevin___/         \

                     \______

_Lisa____            /

         \________/

_Scott___/
```

Clicking on Kevin will result in the following bracket:
```
_Adrian__

         \_Kevin__

_Kevin___/         \

                     \______

_Lisa____           /

         \________/

_Scott___/
```

If you then click on Adrian, then Adrian will replace Kevin in the next round if there is no other matchup:
```
_Adrian__

         \_Adrian__

_Kevin___/         \

                     \______

_Lisa____           /

         \________/

_Scott___/
```

However, if you have the following bracket:
```
_Adrian__

         \_Kevin__

_Kevin___/         \

                     \______

_Lisa____            /

          \__Lisa__/

_Scott___/
```

Then clicking on Adrian will not replace Kevin because that matchup has already been finalized.

If you refresh the page, then the bracket should not be reset, so some backend storage is required.

## Bonus Features

  * A button that resets the tournament back to the starting state
  * Instead of hard coding 16 participants, have a tournament creation state where you can click on empty participant spots to change their names

## Tech Requirements

To get started, fork the this repository onto your machine and develop the app locally. Push any updates to this repository.

You may use any database you are familiar with to store the persistent data. However, we require you to use Node, Express, and GraphQL to serve the data. Thus, you will need to create a GraphQL schema to model all of the data that needs to be exposed. The frontend code must be coded in React. Once the app is complete, deploy it using any cloud service provider and share the url with us.
