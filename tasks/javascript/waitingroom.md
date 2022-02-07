---
title: The waiting room
layout: home
---

## Your task:
Implement a Javascript app (**"Browser"** in the diagram below) with a simple waiting room feature that only allows access to the underlying application until a maximum number of visitors is reached and shows a position in a waiting queue otherwise.  
The position is updated in regular intervals and the visitor is allowed access once there are enough free places.

API endpoint: `https://waitingroom.giantmonkey.de`

You may use a JS framwork (Vue / React / Svelte / Angular) if you like but don't have to.

## Steps:
* Enter waiting room and get a JWT token: `curl -XPOST https://waitingroom.giantmonkey.de/test-shop/enter`
* Check status of position in queue: `curl -H "Authorization: Bearer <jwt>" https://waitingroom.giantmonkey.de/test-shop/check`
* Actively end session: `curl -H "Authorization: Bearer <jwt>" -XDELETE https://waitingroom.giantmonkey.de/test-shop/leave`
* If in queue (`status == “queued”`), show the position to the user and poll the check endpoint to keep it up to date
* If not in queue (`status == “visiting”`), then redirect/allow the user to access the underlying application

![WaitingRoom](https://user-images.githubusercontent.com/71108/152809732-2b2e398f-f32b-44ac-821a-879efa551497.png)

## What we are looking for:
* Process of working documented by concise commits
* Clean, readable code
* Good accessibility
  
## Recommended time
2 - 4 hours
