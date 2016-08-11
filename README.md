### Rules:
Players have the option to join a random room/namespace or create a private room.

Each player logs into the same room/namespace. One player is randomly chosen to be the "picker." The picker is presented with a random hard word from the word-quiz api & can choose to accept the word, or generate a new one until they're given a word they want. The goal is to choose a word difficult enough that they think the other players won't know the true definition.

After the "picker" chooses a word, the chosen word & it's part of speech (looked up from word-graph-dictionary api) is render on all players' screens. The true definition is also pulled from the word-graph-dictionary api & automatically passed into a hidden array of definitions.

All other players then have to enter a made up but plausible definition, which is pushed into the array of definitions. After the last player has submitted a fake definition, the definitions (including the true one) are shuffled & rendered on the page for all players to see. Each player then selects the definition they think is true (not allowed to select their own).

Each player gets a point if their definition is chosen. Continue for 10(?) rounds.

### Technologies
* Node.js, Express, AngularJS
* MongoDB
* socket.io
* Johnny-Five, Tessel-io

To generate random words: https://www.twinword.com/api/word-quiz.php
To generate the actual definition & part of speech of the word chosen by the picker: https://www.twinword.com/api/word-graph-dictionary.php
