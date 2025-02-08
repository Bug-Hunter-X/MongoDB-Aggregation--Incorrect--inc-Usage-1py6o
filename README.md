# MongoDB Aggregation: Incorrect $inc Usage

This repository demonstrates a common error when using the `$inc` operator within MongoDB's aggregation framework. The `$inc` operator is designed to increment a numeric field by a specified value; however, providing it with an array or other non-numeric type will result in unexpected behavior.

The `bug.js` file showcases the problematic code, while `bugSolution.js` presents the corrected implementation.

## Bug Description
The issue arises from attempting to increment the `count` field using an array within the `$addFields` stage.  This results in an error or incorrect results, depending on the MongoDB version.

## Solution
The solution involves directly adding 1 to the `count` field, using standard arithmetic operators within the `$addFields` stage.