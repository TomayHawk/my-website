+++
title = "De Hacks"
date = 2024-08-20T12:37:48+08:00
draft = false
menu = "main"
weight = 60
+++

<!DOCTYPE html>
<html lang="en">

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap">

<style>
    .question-label {
        font-size: 32px; /* Adjust to your desired size */
        font-family: 'Press Start 2P', cursive; /* Pixelated font */
        color: #d3d3d3; /* Optional: Change text color */
        margin: 0;
        flex-wrap: nowrap;
    }

    .custom-label {
        font-size: 16px; /* Adjust to your desired size */
        font-family: 'Press Start 2P', cursive; /* Pixelated font */
        color: #d3d3d3; /* Optional: Change text color */
        margin: 0;
        flex-wrap: nowrap; /* Prevent wrapping */
    }

    .form-question {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -200%); /* Center horizontally and vertically */
        display: flex; /* Use flexbox for horizontal alignment */
        align-items: center; /* Vertically center items */
        flex-wrap: nowrap;
    }

    .form-group {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -0%); /* Center horizontally and vertically */
        display: flex; /* Use flexbox for horizontal alignment */
        align-items: center; /* Vertically center items */
        gap: 10px; /* Space between label and input */
        flex-wrap: nowrap; /* Prevent wrapping */
    }

    .form-control {
        width: 200px; /* Set a specific width */
        flex: none; /* Prevent the input from expanding to fill the available space */
        color: #a9a9a9;
    }
</style>

<div class="fullscreen-background"></div>

<div class="mb-3 form-question">
<label for="exampleFormControlInput1" class="form-label question-label">Question</label>
</div>

<div class="mb-3 form-group">
    <label for="exampleFormControlInput1" class="form-label custom-label">Email address: </label>
    <input type="email" class="form-control bg-dark" id="exampleFormControlInput1" placeholder="name@example.com">
</div>

<div class="mb-3">
  <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
</div>