# gold-mine

An algorithm to solve the "Gold Mine" problem.

# Exercise

Given a gold mine of n \* m dimensions, design an algorithm for a gold miner to collect
as much gold as possible. Each field in this mine contains a positive integer
which is the amount of gold in that space. The miner starts at the first column but can be at any row.
The miner can only move right, diagonally right upwards, or diagonally right downwards. The miner
cannot repeat it's previous move (ie. if it's previous move was diagonally right upwards, it can
only move right or diagonally right downwards on its current move).

![Gold mine diagram](https://i.imgur.com/pmb9XCA.png "Gold Mine Diagram")



# Rules

- If the miner leaves the mine for any reason (goes outside the dimensions of the mine), gold collection
will cease and the final score will be the current score.
- If the miner lands on a section of the mine that has zero gold (an integer value of 0), gold
collection will cease and the final score will be the current score.

# Setup

## Node

1. Install `nvm` via the instructions [here](https://github.com/nvm-sh/nvm#installation-and-update), something like:

```bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/${VERSION}/install.sh | bash
```

2. Install `node 10.16.3` (currently latest LTS):

```bash
nvm install --lts
nvm use --lts
```

4. Upgrade npm and install local dependencies:

```bash
npm install npm@latest -g
npm install
```

## Run

To run the miner through all mines:

```bash
$ npm start
```

This will give you your score per mine, as well as your final score.

To run the miner through a specific mine:

```bash
$ npm run mine -- jupiter
```

This will run the miner through the "jupiter" mine. (All mines can be found
in the `mines/` directory.)

## Run Tests and Lint

To run the tests:

```bash
$ npm run test
```

To run the Lint:

```bash
$ npm run lint
```
