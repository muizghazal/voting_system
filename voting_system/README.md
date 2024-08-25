# Simple Voting System DApp

## Overview

The Simple Voting System DApp allows users to cast votes on various proposals and retrieve information about voters, proposals, and votes. Built using Cartesi’s technology, this system supports vote recording and querying of voting information.

## Features

- **Vote Casting**: Allow users to cast votes on specific proposals.
- **Voter Management**: Keep track of registered voters.
- **Proposal Management**: Manage voting proposals.
- **Result Querying**: Retrieve information about voters, proposals, and votes.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/simple-voting-dapp.git
   cd simple-voting-dapp
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Set Up Environment Variables**

   Create a `.env` file in the root directory and set the `ROLLUP_HTTP_SERVER_URL` variable to your Cartesi Rollup server URL.

   ```env
   ROLLUP_HTTP_SERVER_URL=http://your-rollup-server-url
   ```

4. **Run the DApp**

   ```bash
   node index.js
   ```

## Endpoints

- **Casting Votes**
  - **`POST /advance`**: Submit a vote. The request should include the proposal ID and the vote.

- **Querying Information**
  - **`POST /inspect`**: Retrieve information based on the route. The routes can be:
    - `voters`: List all registered voters.
    - `proposals`: List all proposals (currently not implemented).
    - `votes`: List all recorded votes.

## Code Overview

- **`index.js`**: Contains the main logic for handling voting operations.
  - **`hex2Object(hex)`**: Converts a hexadecimal string to a JavaScript object.
  - **`obj2Hex(obj)`**: Converts a JavaScript object to a hexadecimal string.
  - **`isNumeric(num)`**: Checks if a value is numeric.
  - **`handle_advance(data)`**: Processes and records votes.
  - **`handle_inspect(data)`**: Provides information on voters, proposals, and votes.

## Usage

1. **Cast Votes**

   Use the `/advance` endpoint to submit a vote. The payload should include the `proposalId` and the `vote`.

2. **Query Information**

   Use the `/inspect` endpoint with the appropriate route to retrieve information about voters, proposals, or votes.
# voting_system_dapp
