+++
title = "De Hacks"
date = 2024-09-02T16:47:00+08:00
draft = false
menu = "main"
weight = 60
+++

<!DOCTYPE html>
<html lang="en">

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Nerko+One&display=swap">

<style>
    .fullscreen-background {
        background-image: url('/Flag_Design_-_DA_Developers.png');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        background-color: #000; /* Fallback color if the image fails to load */

        /*  Ensure it covers the entire viewport */
        width: 100%;
        height: 100%;
        position: fixed;
        top: 0;
        left: 0;
        z-index: -1; /*  Send it behind other content */
    }

    .secondary-background {
        background-color: rgba(255, 105, 255, 0.1);
        width: 80%;
        height: 100%;
        position: fixed;
        top: 0;
        left: 10%;
        z-index: -1; /*  Send it behind other content */
    }

    .center-background {
        background-color: rgba(105, 105, 255, 0.35);
        width: 64%;
        height: 100%;
        position: fixed;
        top: 0;
        left: 18%;
        z-index: -1; /*  Send it behind other content */
    }

    .centralized {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%); /* Center horizontally and vertically */
        display: flex;
        align-items: center; /* Vertically center items */
        flex-wrap: nowrap;
        margin: 0;
    }

    .question-container {
        top: 42%;
        left: 50%;
        display: flex;
        flex-wrap: nowrap;
        align-items: center; /* Vertically center items */
        text-align: center; /* Center text horizontally */
        justify-content: center; /* Center contents horizontally */
        width: 60%;
    }

    .question-label {
        font-size: 32px;
        font-family: 'Press Start 2P', cursive;
        color: #d3d3d3;
        flex-wrap: nowrap;
    }

    .subtitle-label {
        font-size: 16px;
        font-family: 'Press Start 2P', cursive;
        color: #aa55bb;
        flex-wrap: nowrap;
    }

    .input-container {
        position: absolute;
        top: 55%;
        right: 40%;
        transform: translate(+0%, -50%); /* Center horizontally and vertically */
        display: flex;
        align-items: center; /* Vertically center items */
        text-align: center; /* Center text horizontally */
        justify-content: center; /* Center contents horizontally */
        flex-wrap: nowrap;
        margin: 0;
        gap: 10px;
    }
    
    .input-container-2 {
        top: 59%;
    }

    .input-container-3 {
        position: absolute;
        top: 54%;
        left: 50%;
        display: flex;
        align-items: center; /* Vertically center items */
        text-align: center; /* Center text horizontally */
        justify-content: center; /* Center contents horizontally */
        flex-wrap: nowrap;
        margin: 0;
    }

    .input-label {
        font-size: 16px; /* Adjust to your desired size */
        font-family: 'Press Start 2P', cursive; /* Pixelated font */
        color: #d3d3d3; /* Optional: Change text color */
        margin: 0;
        width: 90%;
    }

    .input-label-2 {
        width: auto;
    }

    .confirmation-label {
        font-size: 12px; /* Adjust to your desired size */
        font-family: 'Press Start 2P', cursive; /* Pixelated font */
        color: #000000;
    }

    .confirmation-label-2 {
        text-align: right;
        white-space: nowrap;
    }

    .input-control {
        width: 200px; /* Set a specific width */
        flex: none; /* Prevent the input from expanding to fill the available space */
        color: #a9a9a9;
        margin: 0;
    }

    .input-control-long {
        position: relative;
        top: 50%;
        right: 50%;
        width: 800px; /* Width of the textarea */
        min-height: 120px; /* Minimum height of the textarea */
        padding: 10px; /* Padding inside the textarea */
        border: 2px solid #808080; /* Border color */
        border-radius: 5px; /* Rounded corners */
        color: #ffffff; /* Text color */
        background-color: #333333; /* Background color */
        overflow: auto; /* Show scrollbars when content overflows */
        resize: vertical; /* Allow vertical resizing only */
        box-sizing: border-box; /* Include padding and border in width/height calculation */
        white-space: pre-wrap; /* Preserve whitespace and wrap text */
        color: #a9a9a9;
        margin: 0;
    }

    .confirmation-input-container {
        position: absolute;
        top: 15%;
        left: 18%;
        width: 64%;
        display: grid;
        align-items: center; /* Vertically center items */
        grid-template-columns: 3fr 8fr; /* Creates 2 equal-width columns */
        grid-gap: 20px; /* Adjust the spacing between items */
        margin: 0;
    }

    .mc-container {
        position: absolute;
        top: 58%;
        left: 50%;
        transform: translate(-50%, -50%); /* Center horizontally and vertically */
        flex-wrap: nowrap;
        margin: 0;
    }

    .mc-container-2 {
        top: 59.25%;
        left: 54%;
    }

    .mc-container-3 {
        left: 54%;
    }

    .mc-container-4 {
        top: 56%;
        left: 51%;
    }

    .mc-container-5 {
        left: 51%;
    }

    .form-check {
        margin: 10px;
    }

    .form-check-2 {
        margin: 0px;
    }
    
    .form-check-input {
        width: 20px; /* Adjust the size */
        height: 20px; /* Adjust the size */
        margin-right: 30px; /* Adjust the value to your desired margin */
    }

    .form-check-wrapper {
        position: absolute;
        top: 60%;
        left: 50%;
        transform: translate(-50%, -50%); /* Center horizontally and vertically */
        display: flex;
        flex-direction: column; /* Stack child elements vertically */
        gap: 10px; /* Optional: Add space between checkboxes */
        margin: 0;
    }

    .buttons {
        top: 85%;
        justify-content: space-between; /* Space between buttons */
        width: 70%; /* Adjust the width of the container */
        margin: 0 auto; /* Center the container */
    }

    .rounded-button {
        width: 85px;
        font-size: 18px; /* Adjust to your desired size */
        font-family: 'Nerko One', cursive; /* Pixelated font */
        border-radius: 30px; /* Adjust the value to get the desired roundness */
        align-items: center; /* Vertically center items */
        text-align: center; /* Center text horizontally */
        justify-content: center; /* Center contents horizontally */
        white-space: pre;
    }

    .confirmation-button {
        top: 85%;
        width: 340px;
    }

    .custom-bar {
        top: 90%;
        align-items: stretch;
        width: 70%;
    }

    .hide-item {
        visibility: hidden; /* Hides the button but keeps its space in the layout */
    }

    .disable-item {
        display: none;
    }

    @keyframes ease-in-from-above {
        0% {
            transform: translateY(-100%); /* Start above the view */
            opacity: 0; /* Optional: start invisible */
        }
        100% {
            transform: translateY(0); /* End at the original position */
            opacity: 1; /* Optional: end visible */
        }
    }

    @keyframes ease-out-to-below {
        0% {
            transform: translateY(0); /* Start at the current position */
            opacity: 1; /* Fully visible */
        }
        100% {
            transform: translateY(100%); /* Move down */
            opacity: 0; /* Fade out */
        }
    }

    @keyframes ease-in-from-below {
        0% {
            transform: translateY(100%); /* Start below the view */
            opacity: 0; /* Optional: start invisible */
        }
        100% {
            transform: translateY(0); /* End at the original position */
            opacity: 1; /* Optional: end visible */
        }
    }

    @keyframes ease-out-to-above {
        0% {
            transform: translateY(0); /* Start at the current position */
            opacity: 1; /* Fully visible */
        }
        100% {
            transform: translateY(-100%); /* Move up */
            opacity: 0; /* Fade out */
        }
    }

    @keyframes fade-in {
        0% {
            opacity: 0; /* Optional: start invisible */
        }
        100% {
            opacity: 1; /* Optional: end visible */
        }
    }

    @keyframes fade-out {
        0% {
            opacity: 1; /* Fully visible */
        }
        100% {
            opacity: 0; /* Fade out */
        }
    }

    .question-transition {
    }
    
    .question-transition.show1 {
        /* Apply animation */
        opacity: 1;
        animation: ease-in-from-above 0.5s ease-out;
    }
    
    .question-transition.show2 {
        /* Apply animation */
        opacity: 1;
        animation: ease-in-from-below 0.5s ease-out;
    }

    .question-transition.hide1 {
        animation: ease-out-to-below 0.5s ease-out;
        /* Optional: Ensure the element is hidden after the animation */
        opacity: 0;
    }

    .question-transition.hide2 {
        animation: ease-out-to-above 0.5s ease-out;
        /* Optional: Ensure the element is hidden after the animation */
        opacity: 0;
    }

    .input-container.fade-in, .mc-container.fade-in, .input-container-3.fade-in, .secondary-background.fade-in, .center-background.fade-in {
        opacity: 1;
        animation: fade-in 0.5s ease-out;
    }

    .input-container.fade-out, .mc-container.fade-out, .input-container-3.fade-out {
        opacity: 0;
        animation: fade-out 0.5s ease-out;
    }
</style>

<!-- Background -->
<div class="fullscreen-background"></div>

<div class="secondary-background disable-item" id="secondary-background"></div>

<div class="center-background disable-item" id="center-background"></div>

<head>
    <style>
        body{
            margin: 0;
            overflow: hidden;
        }
        html,body{
            height: 100%;
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    <script src="particles.min.js"></script>
    <script src="app.js"></script>
</body>

<!-- Question 1 -->
<div class="centralized question-container" id="Q0">
    <div class="question-transition" id="T0">
        <label class="form-label question-label">What is your Full Name?</label>
    </div>
</div>
<div class="input-container" id="A0">
    <label class="form-label input-label">Full Name: </label>
    <input type="text" class="input-control bg-dark" placeholder="Mike Tyson" id="fullName">
</div>
<div class="input-container input-container-2" id="A100">
    <label class="form-label input-label">Preferred Name: </label>
    <input type="text" class="input-control bg-dark" placeholder="Mike Tyson" id="preferredName">
</div>
<!-- Question 2 -->
<div class="centralized question-container disable-item" id="Q1">
    <div class="question-transition" id="T1">
        <label class="form-label question-label">What is your email address?</label>
    </div>
</div>
<div class="input-container disable-item" id="A1">
    <label class="form-label input-label">Email: </label>
    <input type="email" class="input-control bg-dark" placeholder="name@example.com" id="emailAddress">
</div>
<!-- Question 3 -->
<div class="centralized question-container disable-item" id="Q2">
    <div class="question-transition" id="T2">
        <label class="form-label question-label">What is your FHDA CWID?</label>
        <label class="form-label subtitle-label">This is your FHDA MyPortal ID.</label>
    </div>
</div>
<div class="input-container disable-item" id="A2">
    <label class="form-label input-label">FHDA CWID: </label>
    <input type="text" class="input-control bg-dark" placeholder="01234567" id="idNumber">
</div>
<!-- Question 4 -->
<div class="centralized question-container disable-item" id="Q3">
    <div class="question-transition" id="T3">
        <label class="form-label question-label">Are you current an FHDA student?</label>
    </div>
</div>
<!-- Multiple Choice -->
<div class="mc-container mc-container-2 disable-item" id="A3">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="radioDeAnza">
        <label class="form-check-label input-label" for="radioDeAnza">Yes, I study at De Anza College.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="radioFoothil">
        <label class="form-check-label input-label" for="radioFoothil">Yes, I study at Foothill College.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="radioAlumni">
        <label class="form-check-label input-label" for="radioAlumni">No, I am an FHDA Alumni.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="radioNeverAttended">
        <label class="form-check-label input-label" for="radioNeverAttended">No, I have never attended Foothill/De Anza College.</label>
    </div>
</div>
<!-- Question 5 -->
<div class="centralized question-container disable-item" id="Q4">
    <div class="question-transition" id="T4">
        <label class="form-label question-label">What year of study are you in?</label>
        <label class="form-label subtitle-label">Please select 'First Year' if this does not apply to you.</label>
    </div>
</div>
<div class="mc-container mc-container-3 disable-item" id="A4">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="radioFirstYear">
        <label class="form-check-label input-label input-label-2" for="radioFirstYear">First Year</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="radioSecondYear">
        <label class="form-check-label input-label input-label-2" for="radioSecondYear">Second Year</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="radioThirdYear">
        <label class="form-check-label input-label input-label-2" for="radioThirdYear">Third Year</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="radioFourthYear">
        <label class="form-check-label input-label input-label-2" for="radioFourthYear">Fourth Year or Higher</label>
    </div>
</div>
<!-- Question 6 -->
<div class="centralized question-container disable-item" id="Q5">
    <div class="question-transition" id="T5">
        <label class="form-label question-label">What is your major?</label>
        <label class="form-label subtitle-label">Please enter '-' if this does not apply to you.</label>
    </div>
</div>
<div class="input-container disable-item" id="A5">
    <label class="form-label input-label">Major: </label>
    <input type="text" class="input-control bg-dark" placeholder="Computer Science" id="major">
</div>
<!-- Question 7 -->
<div class="centralized question-container disable-item" id="Q6">
    <div class="question-transition" id="T6">
        <label class="form-label question-label">What is your skill level?</label>
    </div>
</div>
<div class="mc-container mc-container-4 disable-item" id="A6">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA6" id="radioBeginner">
        <label class="form-check-label input-label input-label-2" for="radioBeginner">Beginner</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA6" id="radioIntermediate">
        <label class="form-check-label input-label input-label-2" for="radioIntermediate">Intermediate</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA6" id="radioAdvanced">
        <label class="form-check-label input-label input-label-2" for="radioAdvanced">Advanced</label>
    </div>
</div>
<!-- Question 8 -->
<div class="centralized question-container disable-item" id="Q7">
    <div class="question-transition" id="T7">
        <label class="form-label question-label">How many hackathons have you been a part of?</label>
    </div>
</div>
<div class="mc-container disable-item" id="A7">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="radioZeroHackathons">
        <label class="form-check-label input-label input-label-2" for="radioZeroHackathons">0</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="radioOneHackathon">
        <label class="form-check-label input-label input-label-2" for="radioOneHackathon">1-2</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="radioThreeHackathons">
        <label class="form-check-label input-label input-label-2" for="radioThreeHackathons">3+</label>
    </div>
</div>
<!-- Question 9 -->
<div class="centralized question-container disable-item" id="Q8">
    <div class="question-transition" id="T8">
        <label class="form-label question-label">Do you have any dietary restrictions?</label>
    </div>
</div>
<!-- Checkboxes -->
<div class="form-check-wrapper mc-container disable-item" id="A8">
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="checkVegetarian">
        <label class="form-check-label input-label input-label-2" for="checkVegetarian">Vegetarian</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="checkHalal">
        <label class="form-check-label input-label input-label-2" for="checkHalal">Halal</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="checkGlutenFree">
        <label class="form-check-label input-label input-label-2" for="checkGlutenFree">Gluten-free</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="checkOthers">
        <label class="form-check-label input-label input-label-2" for="checkOthers">Others: </label>
        <input type="text" class="input-control bg-dark" placeholder="..." for="checkOthers" id="checkOthersText">
    </div>
</div>
<!-- Question 10 -->
<div class="centralized question-container disable-item" id="Q9">
    <div class="question-transition" id="T9">
        <label class="form-label question-label">Do you have any additional accommodational needs?</label>
    </div>
</div>
<div class="input-container-3 disable-item" id="A9">
    <textarea class="input-control-long bg-dark" id="accommodationNeeds"></textarea>
</div>
<!-- Question 11 -->
<div class="centralized question-container disable-item" id="Q10">
    <div class="question-transition" id="T10">
        <label class="form-label question-label">What is your T-Shirt Size?</label>
    </div>
</div>
<div class="mc-container mc-container-5 disable-item" id="A10">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="radioSmall">
        <label class="form-check-label input-label input-label-2" for="radioSmall">Small (S)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="radioMedium">
        <label class="form-check-label input-label input-label-2" for="radioMedium">Medium (M)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="radioLarge">
        <label class="form-check-label input-label input-label-2" for="radioLarge">Large (L)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="radioExtraLarge">
        <label class="form-check-label input-label input-label-2" for="radioExtraLarge">Extra Large (XL)</label>
    </div>
</div>
<!-- Question 12 -->
<div class="centralized question-container disable-item" id="Q11">
    <div class="question-transition" id="T11">
        <label class="form-label question-label">Will you have access to a computer during the hackathon?</label>
    </div>
</div>
<div class="mc-container mc-container-2 disable-item" id="A11">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="radioHaveLaptop">
        <label class="form-check-label input-label input-label-2" for="radioHaveLaptop">I have a laptop that I can code/work on.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="radioHaveDesktop">
        <label class="form-check-label input-label input-label-2" for="radioHaveDesktop">I will bring a desktop computer to the event.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="radioBadComputer">
        <label class="form-check-label input-label input-label-2" for="radioBadComputer">I will not have access to a "good" computer.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="radioNoComputer">
        <label class="form-check-label input-label input-label-2" for="radioNoComputer">I will not have access to a computer.</label>
    </div>
</div>
<!-- Question 13 -->
<div class="centralized question-container disable-item" id="Q12">
    <div class="question-transition" id="T12">
        <label class="form-label question-label">Why are you attending DAHacks 3.0?</label>
    </div>
</div>
<div class="input-container-3 disable-item" id="A12">
    <textarea class="input-control-long bg-dark" id="attendReason"></textarea>
</div>
<!-- Question 14 -->
<div class="centralized question-container disable-item" id="Q13">
    <div class="question-transition" id="T13">
    <label class="form-label question-label">What additional information would you like us to know?</label>
    <label class="form-label subtitle-label">Feel free to include any significant coding or hackathon experiences below!</label>
    </div>
</div>
<div class="input-container-3 disable-item" id="A13">
    <textarea class="input-control-long bg-dark" id="additionalInformation"></textarea>
</div>

<div class="confirmation-input-container disable-item" id="confirmationContainer">
    <label class="form-label input-label confirmation-label confirmation-label-2">Full Name: </label>
    <label class="form-label input-label confirmation-label" id="fullNameConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Preferred Name: </label>
    <label class="form-label input-label confirmation-label" id="preferredNameConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Email Address: </label>
    <label class="form-label input-label confirmation-label" id="emailConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">FHDA CWID: </label>
    <label class="form-label input-label confirmation-label" id="idConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Current Status: </label>
    <label class="form-label input-label confirmation-label" id="statusConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Year: </label>
    <label class="form-label input-label confirmation-label" id="yearConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Major: </label>
    <label class="form-label input-label confirmation-label" id="majorConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Experience: </label>
    <label class="form-label input-label confirmation-label" id="experienceConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Hackathon Experience: </label>
    <label class="form-label input-label confirmation-label" id="hackathonExperienceConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Dietary Preferences: </label>
    <label class="form-label input-label confirmation-label" id="dietaryPreferencesConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Accommodation Needs: </label>
    <label class="form-label input-label confirmation-label" id="accommodationNeedsConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Shirt Size: </label>
    <label class="form-label input-label confirmation-label" id="shirtSizeConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Computer Availability: </label>
    <label class="form-label input-label confirmation-label" id="computerConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Reason for Attending: </label>
    <label class="form-label input-label confirmation-label" id="attendReasonConfirmation"></label>
    <label class="form-label input-label confirmation-label confirmation-label-2">Additional Information: </label>
    <label class="form-label input-label confirmation-label" id="additionalInformationConfirmation"></label>
</div>

<!-- Buttons -->
<div class="centralized buttons">
    <button type="button" class="btn btn-info rounded-button hide-item" id="prevButton" onclick="prevQuestion()">< Back  </button>
    <button type="button" class="btn btn-info rounded-button" disabled id="nextButton" onclick="nextQuestion()">  Next ></button>
    <button type="button" class="btn btn-success rounded-button disable-item" id="submitButton" onclick="submitPressed()">Submit</button>
</div>

<button type="button" class="btn btn-warning centralized rounded-button confirmation-button disable-item" id="confirmButton" onclick="confirmPressed()">Confirm Submission</button>

<!-- Progress Bar -->
<div class="progress centralized custom-bar" role="progressbar" aria-label="Basic example" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
    <div class="progress-bar" id="progressBar" style="width: 7.14%"></div>
</div>

<script>
    // Current question index
    const questionCount = 14;
    let lastAnsweredIndex = 0;
    let holes = new Array();

    let currentIndex = 0;
    let prevIndex = 0;
    
    let nextButton = document.getElementById('nextButton');

    function displayQuestion() {
        document.getElementById('prevButton').disabled = true;
        document.getElementById('nextButton').disabled = true;
        document.getElementById('submitButton').disabled = true;

        const prevQuestionElement = document.getElementById(`T${prevIndex}`);
        const nextQuestionElement = document.getElementById(`T${currentIndex}`);

        document.getElementById(`Q${currentIndex}`).classList.remove('disable-item');
        document.getElementById(`A${currentIndex}`).classList.remove('disable-item');

        // Hide current question with animation
        if (prevIndex < currentIndex) {
            prevQuestionElement.classList.add('hide1');
            nextQuestionElement.classList.add('show1');
        } else {
            if ((prevIndex !== (questionCount - 1)) || (currentIndex !== (questionCount - 1))) { prevQuestionElement.classList.add('hide2'); }
            nextQuestionElement.classList.add('show2');
        }

        if ((prevIndex !== (questionCount - 1)) || (currentIndex !== (questionCount - 1))) { document.getElementById(`A${prevIndex}`).classList.add('fade-out'); }
        document.getElementById(`A${currentIndex}`).classList.add('fade-in')

        if (currentIndex === 0) {
            document.getElementById(`A100`).classList.add('fade-in')
        } else if (prevIndex === 0) {
            document.getElementById(`A100`).classList.add('fade-out')
        }

        // Update buttons
        document.getElementById('prevButton').classList.toggle('hide-item', currentIndex === 0);
        document.getElementById('nextButton').classList.toggle('disable-item', currentIndex === questionCount - 1);
        document.getElementById('submitButton').classList.toggle('disable-item', currentIndex !== questionCount - 1);

        // Update progress bar
        document.getElementById('progressBar').style.width = `${((currentIndex + 1) / questionCount) * 100}%`;

        // Wait for the animation to finish
        setTimeout(() => {
            prevQuestionElement.classList.remove('hide1');
            nextQuestionElement.classList.remove('show1');

            prevQuestionElement.classList.remove('hide2');
            nextQuestionElement.classList.remove('show2');

            document.getElementById(`A${prevIndex}`).classList.remove('fade-out')
            document.getElementById(`A${currentIndex}`).classList.remove('fade-in')

            document.getElementById(`A100`).classList.remove('fade-in')
            document.getElementById(`A100`).classList.remove('fade-out')

            // Hide all containers
            document.querySelectorAll('.question-container, .input-container, .mc-container, .input-container-3').forEach(container => container.classList.add('disable-item'));

            // Show appropriate container
            document.getElementById(`Q${currentIndex}`).classList.remove('disable-item');
            document.getElementById(`A${currentIndex}`).classList.remove('disable-item');
            if (currentIndex === 0) {document.getElementById('A100').classList.remove('disable-item');}

            document.getElementById('prevButton').disabled = false;
            document.getElementById('nextButton').disabled = false;
            document.getElementById('submitButton').disabled = false;

            if (currentIndex > lastAnsweredIndex) {
                lastAnsweredIndex = currentIndex - 1;
                nextButton.disabled = true;
                if ([8, 9, 13].includes(currentIndex)) {
                    nextButton.disabled = false; // Disable the button if the input is empty
                }
            } else if (holes.includes(currentIndex)) {
                nextButton.disabled = true;
            }

        }, 500); // Match the duration of the hide animation
    }

    // Add event listeners to input fields
    document.querySelectorAll('.input-control, .form-check-input, .input-control-long').forEach( input => {
        input.addEventListener('input', function() {
            if (this.value.trim().length > 0 || [8, 9, 13].includes(currentIndex)) {
                if (holes.indexOf(currentIndex) > -1) {
                    holes = holes.filter(index => index !== currentIndex);
                }
                nextButton.disabled = false; // Enable the button when the input is filled
                if (currentIndex === 0) {
                    if ((document.getElementById('fullName').value.trim().length == 0) || (document.getElementById('preferredName').value.trim().length == 0)) {
                        nextButton.disabled = true; // Disable the button if the input is empty
                    }
                }
            } else {
                nextButton.disabled = true; // Disable the button if the input is empty
                holes.push(currentIndex);
            }
    })});

    document.getElementById('checkOthersText').addEventListener('input', function() {
         if (this.value.trim().length > 0) {
            checkOthers.checked = true;
         } else {
            checkOthers.checked = false;
         }
    })

    function nextQuestion() {
        if (currentIndex < questionCount - 1) {
            prevIndex = currentIndex;
            currentIndex++;
            displayQuestion();
            if (currentIndex > lastAnsweredIndex) {
                lastAnsweredIndex = currentIndex - 1;
                nextButton.disabled = true;
                if ([8, 9, 13].includes(currentIndex)) {
                    nextButton.disabled = false; // Disable the button if the input is empty
                }
            } else if (holes.includes(currentIndex)) {
                nextButton.disabled = true;
            }
        }
    }

    function prevQuestion() {
        if (currentIndex > 0) {
            prevIndex = currentIndex;
            currentIndex--;
            if (!document.getElementById(`confirmationContainer`).classList.contains('disable-item')) {
                document.getElementById(`confirmationContainer`).classList.add('disable-item');
                document.getElementById('confirmButton').classList.add('disable-item');
                document.getElementById('secondary-background').classList.add('disable-item');
                document.getElementById('center-background').classList.add('disable-item');
                currentIndex++;
            }
            displayQuestion();
            nextButton.disabled = false;
        }
    }

    function submitPressed() {
        // Hide all containers
        document.querySelectorAll('.question-container, .input-container, .mc-container, .input-container-3').forEach(container => container.classList.add('disable-item'));
        document.getElementById('nextButton').classList.add('disable-item');
        document.getElementById('submitButton').classList.add('disable-item');
        document.getElementById('confirmButton').classList.remove('disable-item');
        document.getElementById('secondary-background').classList.remove('disable-item');
        document.getElementById('center-background').classList.remove('disable-item');
        
        document.getElementById('secondary-background').classList.add('fade-in');
        document.getElementById('center-background').classList.add('fade-in');

        setTimeout(() => {
            document.getElementById('secondary-background').classList.remove('fade-in');
            document.getElementById('center-background').classList.remove('fade-in');
        }, 500);

        document.getElementById(`confirmationContainer`).classList.remove('disable-item');

        document.getElementById('fullNameConfirmation').textContent = document.getElementById('fullName').value;
        document.getElementById('preferredNameConfirmation').textContent = document.getElementById('preferredName').value;
        document.getElementById('emailConfirmation').textContent = document.getElementById('emailAddress').value;
        document.getElementById('idConfirmation').textContent = document.getElementById('idNumber').value;

        // Update status based on radio buttons
        if (radioDeAnza.checked) { document.getElementById('statusConfirmation').textContent = "Yes, I study at De Anza College."; }
        else if (radioFoothill.checked) { document.getElementById('statusConfirmation').textContent = "Yes, I study at Foothill College."; }
        else if (radioAlumni.checked) { document.getElementById('statusConfirmation').textContent = "No, I am an FHDA Alumni."; }
        else if (radioNeverAttended.checked) { document.getElementById('statusConfirmation').textContent = "No, I have never attended Foothill/De Anza College."; }

        // Update year based on radio buttons
        if (radioFirstYear.checked) { document.getElementById('yearConfirmation').textContent = "First Year"; }
        else if (radioSecondYear.checked) { document.getElementById('yearConfirmation').textContent = "Second Year"; }
        else if (radioThirdYear.checked) { document.getElementById('yearConfirmation').textContent = "Third Year"; }
        else if (radioFourthYear.checked) { document.getElementById('yearConfirmation').textContent = "Fourth Year or Higher"; }

        document.getElementById('majorConfirmation').textContent = document.getElementById('major').value;

        // Update experience based on radio buttons
        if (radioBeginner.checked) { document.getElementById('experienceConfirmation').textContent = "Beginner"; }
        else if (radioIntermediate.checked) { document.getElementById('experienceConfirmation').textContent = "Intermediate"; }
        else if (radioAdvanced.checked) { document.getElementById('experienceConfirmation').textContent = "Advanced"; }

        // Update hackathon experience based on radio buttons
        if (radioZeroHackathons.checked) { document.getElementById('hackathonExperienceConfirmation').textContent = "None"; }
        else if (radioOneHackathon.checked) { document.getElementById('hackathonExperienceConfirmation').textContent = "1-2"; }
        else if (radioThreeHackathons.checked) { document.getElementById('hackathonExperienceConfirmation').textContent = "3+"; }

        // Update dietary preferences based on checkboxes
        let dietaryPreferences = [];
        if (checkVegetarian.checked) { dietaryPreferences.push("Vegetarian"); }
        if (checkHalal.checked) { dietaryPreferences.push("Halal"); }
        if (checkGlutenFree.checked) { dietaryPreferences.push("Gluten-Free"); }
        if (checkOthers.checked) { dietaryPreferences.push(checkOthersText.value); }
        document.getElementById('dietaryPreferencesConfirmation').textContent = dietaryPreferences.join(", ");

        document.getElementById('accommodationNeedsConfirmation').textContent = document.getElementById('accommodationNeeds').value;

        // Update shirt size based on radio buttons
        if (radioSmall.checked) { document.getElementById('shirtSizeConfirmation').textContent = "Small (S)"; }
        else if (radioMedium.checked) { document.getElementById('shirtSizeConfirmation').textContent = "Medium (M)"; }
        else if (radioLarge.checked) { document.getElementById('shirtSizeConfirmation').textContent = "Large (L)"; }
        else if (radioExtraLarge.checked) { document.getElementById('shirtSizeConfirmation').textContent = "Extra Large (XL)"; }

        // Update computer availability based on radio buttons
        if (radioHaveLaptop.checked) { document.getElementById('computerConfirmation').textContent = "I have a laptop that I can code/work on."; }
        else if (radioHaveDesktop.checked) { document.getElementById('computerConfirmation').textContent = "I will bring a desktop computer to the event. (Why???)"; }
        else if (radioBadComputer.checked) { document.getElementById('computerConfirmation').textContent = "I will not have access to a 'good' computer."; }
        else if (radioNoComputer.checked) { document.getElementById('computerConfirmation').textContent = "I will not have access to a computer."; }

        document.getElementById('attendReasonConfirmation').textContent = document.getElementById('attendReason').value;
        document.getElementById('additionalInformationConfirmation').textContent = document.getElementById('additionalInformation').value;
    }

    function confirmPressed() {
        alert("Submission Confirmed");
    }
</script>
