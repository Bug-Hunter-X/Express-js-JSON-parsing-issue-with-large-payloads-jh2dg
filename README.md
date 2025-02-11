# Express.js JSON Parsing Issue with Large Payloads

This repository demonstrates a bug in an Express.js application where parsing large JSON payloads fails. The application uses the `express.json()` middleware to parse incoming JSON data, but it encounters an issue when processing large JSON objects. This issue manifests as the `req.body` remaining empty or incomplete.

## Bug Description
The `express.json()` middleware has a default limit on the size of JSON payloads it can parse. When a payload exceeds this limit, the request body is not parsed correctly, resulting in unexpected behavior.

## Solution
The solution involves configuring the `express.json()` middleware to increase the size limit for incoming JSON payloads.