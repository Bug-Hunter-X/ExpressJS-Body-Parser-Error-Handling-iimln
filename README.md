# Express.js JSON Body Parsing Failure

This repository demonstrates a common issue encountered when working with JSON request bodies in Express.js applications.  The problem stems from the incorrect or missing configuration of middleware responsible for parsing JSON payloads.

## Bug Description

The provided code uses `express.json()` but fails to correctly parse the incoming JSON data. `req.body` remains empty despite the client sending valid JSON.

## Solution

The solution involves ensuring that `express.json()` is correctly placed in the middleware stack *before* any routes that expect JSON data. The solution also shows how to handle errors in the middleware using try...catch block.