Here's a sample README file in text format for your GitHub project:

markdown
Copy code
# Shamir's Secret Sharing - Simplified Implementation

## Overview

This repository contains an implementation of a simplified version of Shamir's Secret Sharing algorithm. The algorithm allows for the sharing of a secret, represented by the constant term \( c \) of a polynomial, using roots provided in a specified format.

## Problem Statement

Given an unknown polynomial of degree \( m \) represented as:

\[ f(x) = a_m x^m + a_{m-1} x^{m-1} + ... + a_1 x + c \]

Where \( m \) is the degree of the polynomial and \( c \) is the constant term, the objective is to find \( c \) using roots encoded in various bases.

## Input Format

The input is provided in JSON format containing:
- n: The number of roots provided.
- k: The minimum number of roots required to solve for the polynomial's coefficients.
- Each root is represented with:
  - base: The base in which the value is encoded.
  - value: The encoded value.

### Example Input

```json
{
    "keys": {
        "n": 4,
        "k": 3
    },
    "1": {
        "base": "10",
        "value": "4"
    },
    "2": {
        "base": "2",
        "value": "111"
    },
    "3": {
        "base": "10",
        "value": "12"
    },
    "6": {
        "base": "4",
        "value": "213"
    }
}
Implementation Steps
Read the Test Case from JSON File: Parse and read input provided in JSON format.
Decode the Y Values: Convert the encoded Y values from their respective bases to integers.
Find the Secret (C): Calculate the constant term 
𝑐
c using known methods such as Lagrange interpolation, matrix methods, or Gaussian elimination.
