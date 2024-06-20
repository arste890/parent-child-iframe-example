# Parent-Child Iframe Communication Repository

This repository contains code that establishes a parent-child iframe relationship. The code runs a `postMessage` script on both the parent and child HTML documents.

## Overview

The main purpose of this code is to enable the parent frame to request the height of the child frame's contents. This allows the parent to automatically adjust the iframe to the appropriate size, ensuring a seamless user experience.

## How it Works

The `postMessage` method is used to safely enable cross-origin communication. Normally, scripts on different pages are allowed to access each other if and only if the pages they originate from share the same protocol, port number, and host (also known as the "same-origin policy").

`postMessage` provides a controlled mechanism to circumvent this restriction in a way which is secure when properly used.

## Usage

1. **Parent Document**: The parent document contains the iframe and sends a `postMessage` to the child document, requesting the content height.

2. **Child Document**: The child document listens for the `postMessage` event. When the event is fired, it calculates its content height and sends it back to the parent document using `postMessage`.

3. **Parent Document**: The parent document listens for the `postMessage` event. When the event is fired, it receives the content height from the child document and adjusts the iframe height accordingly.
