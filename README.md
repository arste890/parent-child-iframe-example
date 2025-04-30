
# Parent-Child Iframe Communication Repository

[![License: StevensIT License v1.0](https://img.shields.io/badge/License-StevensIT%20License%20v1.0-F7F5F0?style=flat-square&logoColor=white&labelColor=191F27)](./LICENSE)
![Built With: HTML](https://img.shields.io/badge/Built%20with-HTML-0A0A23?style=flat-square&logo=html5&logoColor=white&labelColor=0A0A23)
![Status: Maintained](https://img.shields.io/badge/status-maintained-0A0A23?style=flat-square&labelColor=0A0A23&color=4CAF50)
![Open Issues](https://img.shields.io/github/issues/arste890/parent-child-iframe-example?style=flat-square&labelColor=0A0A23)
![Last Commit](https://img.shields.io/github/last-commit/arste890/parent-child-iframe-example?style=flat-square&labelColor=0A0A23)
![Repo Size](https://img.shields.io/github/repo-size/arste890/parent-child-iframe-example?style=flat-square&labelColor=0A0A23)

<a href="./LICENSE">
  <img src="https://github.com/arste890/SAC/blob/main/StevensIT-Logo.png?raw=true" alt="StevensIT Logo" width="120"/>
</a>

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

## License & Attribution

All contents of this repository are licensed under the **StevensIT License v1.0**.  
Commercial use, sublicensing, redistribution, or modification for profit is **strictly prohibited** without prior written permission.  
Any permitted use must include proper attribution:

> "Developed by StevensIT, a Division of StevensED LLC. Used under the StevensIT License v1.0."

Please refer to the [LICENSE](./LICENSE.md) file for full terms and conditions.

## Contact

To request commercial licensing or obtain written permission for broader use, please contact:

**StevensIT**  
Email: report@StevensED.org  
Website: [IT.StevensED.org](https://IT.StevensED.org)

---

© 2025 | StevensED LLC | StevensIT | All rights reserved.
