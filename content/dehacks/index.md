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
        white-space: pre;
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
</style>

<!-- Background -->
<div class="fullscreen-background"></div>

<!-- Question -->


<!-- Question 1 -->
<div class="centralized question-container" id="Q0">
    <label class="form-label question-label" id="questionLabel">What is your Full Name?</label>
</div>
<div class="input-container" id="A0">
    <label class="form-label input-label">Full Name: </label>
    <input type="text" class="input-control bg-dark" placeholder="Mike Tyson">
</div>
<div class="input-container input-container-2" id="A100">
    <label class="form-label input-label">Preferred Name: </label>
    <input type="text" class="input-control bg-dark" placeholder="Mike Tyson">
</div>
<!-- Question 2 -->
<div class="centralized question-container disable-item" id="Q1">
    <label class="form-label question-label" id="questionLabel">What is your email address?</label>
</div>
<div class="input-container disable-item" id="A1">
    <label class="form-label input-label">Email: </label>
    <input type="email" class="input-control bg-dark" placeholder="name@example.com">
</div>
<!-- Question 3 -->
<div class="centralized question-container disable-item" id="Q2">
    <label class="form-label question-label" id="questionLabel">What is your FHDA CWID?</label>
</div>
<div class="input-container disable-item" id="A2">
    <label class="form-label input-label">FHDA CWID: </label>
    <input type="text" class="input-control bg-dark" placeholder="01234567">
</div>
<!-- Question 4 -->
<div class="centralized question-container disable-item" id="Q3">
    <label class="form-label question-label" id="questionLabel">Are you current an FHDA student?</label>
</div>
<!-- Multiple Choice -->
<div class="mc-container mc-container-2 disable-item" id="A3">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="flexRadioDefault1">
        <label class="form-check-label input-label" for="flexRadioDefault1">Yes, I study at De Anza College.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="flexRadioDefault1">
        <label class="form-check-label input-label" for="flexRadioDefault1">Yes, I study at Foothill College.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="flexRadioDefault1">
        <label class="form-check-label input-label" for="flexRadioDefault1">No, I am an FHDA Alumni.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA3" id="flexRadioDefault1">
        <label class="form-check-label input-label" for="flexRadioDefault1">No, I have never attended Foothill/De Anza College.</label>
    </div>
</div>
<!-- Question 5 -->
<div class="centralized question-container disable-item" id="Q4">
    <label class="form-label question-label" id="questionLabel">What year of study are you in?</label>
</div>
<div class="mc-container mc-container-3 disable-item" id="A4">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">First year.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Second year.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Third year.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA4" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Fourth year or higher.</label>
    </div>
</div>
<!-- Question 6 -->
<div class="centralized question-container disable-item" id="Q5">
    <label class="form-label question-label" id="questionLabel">What is your major?</label>
</div>
<div class="input-container disable-item" id="A5">
    <label class="form-label input-label">Major: </label>
    <input type="text" class="input-control bg-dark" placeholder="Computer Science">
</div>
<!-- Question 7 -->
<div class="centralized question-container disable-item" id="Q6">
    <label class="form-label question-label" id="questionLabel">What is your skill level?</label>
</div>
<div class="mc-container mc-container-4 disable-item" id="A6">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA6" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Beginner.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA6" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Intermediate.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioflexRadioA6Default" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Advanced.</label>
    </div>
</div>
<!-- Question 8 -->
<div class="centralized question-container disable-item" id="Q7">
    <label class="form-label question-label" id="questionLabel">How many hackathons have you been a part of?</label>
</div>
<div class="mc-container disable-item" id="A7">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">0.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">1-2.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA7" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">3+.</label>
    </div>
</div>
<!-- Question 9 -->
<div class="centralized question-container disable-item" id="Q8">
    <label class="form-label question-label" id="questionLabel">Do you have any dietary restrictions?</label>
</div>
<!-- Checkboxes -->
<div class="form-check-wrapper mc-container disable-item" id="A8">
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
        <label class="form-check-label input-label input-label-2" for="flexCheckDefault">Vegetarian</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked">
        <label class="form-check-label input-label input-label-2" for="flexCheckChecked">Vegan</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked">
        <label class="form-check-label input-label input-label-2" for="flexCheckChecked">Gluten-free</label>
    </div>
    <div class="form-check form-check-2">
        <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked">
        <label class="form-check-label input-label input-label-2" for="flexCheckChecked">Others: </label>
    </div>
</div>
<!-- Question 10 -->
<div class="centralized question-container disable-item" id="Q9">
    <label class="form-label question-label" id="questionLabel">Do you have any additional accommodational needs?</label>
</div>
<div class="input-container-3 disable-item" id="A9">
    <textarea class="input-control-long bg-dark"></textarea>
</div>
<!-- Question 11 -->
<div class="centralized question-container disable-item" id="Q10">
    <label class="form-label question-label" id="questionLabel">What is your T-Shirt Size?</label>
</div>
<div class="mc-container mc-container-5 disable-item" id="A10">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Small. (S)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Medium. (M)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Large. (L)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA10" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">Extra Large. (XL)</label>
    </div>
</div>
<!-- Question 12 -->
<div class="centralized question-container disable-item" id="Q11">
    <label class="form-label question-label" id="questionLabel">Will you have access to a computer during the hackathon?</label>
</div>
<div class="mc-container mc-container-2 disable-item" id="A11">
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">I have a laptop that I can code/work on.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">I will bring a desktop computer to the event. (Why???)</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">I will not have access to a "good" computer.</label>
    </div>
    <div class="form-check">
        <input class="form-check-input bg-secondary" type="radio" name="flexRadioA11" id="flexRadioDefault1">
        <label class="form-check-label input-label input-label-2" for="flexRadioDefault1">I will not have access to a computer.</label>
    </div>
</div>
<!-- Question 13 -->
<div class="centralized question-container disable-item" id="Q12">
    <label class="form-label question-label" id="questionLabel">Why are you attending DAHacks 3.0?</label>
</div>
<div class="input-container-3 disable-item" id="A12">
    <textarea class="input-control-long bg-dark"></textarea>
</div>
<!-- Question 14 -->
<div class="centralized question-container disable-item" id="Q13">
    <label class="form-label question-label" id="questionLabel">What additional information would you like us to know? Feel free to include any significant coding or hackathon experiences below!</label>
</div>
<div class="input-container-3 disable-item" id="A13">
    <textarea class="input-control-long bg-dark"></textarea>
</div>

<!-- Input -->

<!-- Buttons -->
<div class="centralized buttons">
    <button type="button" class="btn btn-info rounded-button hide-item" id="prevButton" onclick="prevQuestion()">< Back  </button>
    <button type="button" class="btn btn-info rounded-button" id="nextButton" onclick="nextQuestion()">  Next ></button>
    <button type="button" class="btn btn-success rounded-button disable-item" id="submitButton" onclick="submitPressed()">Submit</button>
</div>

<!-- Progress Bar -->
<div class="progress centralized custom-bar" role="progressbar" aria-label="Basic example" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">
    <div class="progress-bar" id="progressBar" style="width: 7.14%"></div>
</div>

<script>
    // Current question index
    let currentIndex = 0;
    let prevIndex = 0;
    let canProceed = false;
    const questionCount = 13;

    function displayQuestion() {
        /*
        const prevQuestionElement = document.getElementById(`Q${prevIndex}`);
        const nextQuestionElement = document.getElementById(`Q${currentIndex}`);

        // Reset transform before applying new class
        prevQuestionElement.style.transform = '';
        nextQuestionElement.style.transform = '';

        // Apply the appropriate transform based on the direction
        if (prevIndex < currentIndex) {
            prevQuestionElement.classList.add('slide-transition', 'slide-exit-active');
            prevQuestionElement.style.transform = 'translateY(300px)';
            nextQuestionElement.classList.add('slide-transition', 'slide-enter-active');
            nextQuestionElement.style.transform = 'translateY(-300px)';
        } else {
            prevQuestionElement.classList.add('slide-transition', 'slide-exit-active');
            prevQuestionElement.style.transform = 'translateY(-300px)';
            nextQuestionElement.classList.add('slide-transition', 'slide-enter-active');
            nextQuestionElement.style.transform = 'translateY(300px)';
        }
        */

        
        // Hide all containers
        document.querySelectorAll('.input-container, .mc-container, .form-check-wrapper, .question-container, .input-container-3').forEach(container => container.classList.add('disable-item'));

        // Show appropriate container
        document.getElementById(`Q${currentIndex}`).classList.remove('disable-item');
        document.getElementById(`A${currentIndex}`).classList.remove('disable-item');
        if (currentIndex === 0) {document.getElementById('A100').classList.remove('disable-item');}
        

        // Update buttons
        document.getElementById('prevButton').classList.toggle('hide-item', currentIndex === 0);
        document.getElementById('nextButton').classList.toggle('disable-item', currentIndex === questionCount - 1);
        document.getElementById('submitButton').classList.toggle('disable-item', currentIndex !== questionCount - 1);

        // Update progress bar
        document.getElementById('progressBar').style.width = `${((currentIndex + 1) / questionCount) * 100}%`;
    }

    /*
    // Function to check input fields and toggle buttons
    function checkInputs() {
        // Get all input fields
        const inputs = document.querySelectorAll('.input-container input');
    
        // Check if any input field has a value
        const hasInput = Array.from(inputs).some(input => input.value.trim() !== '');

        // Get the buttons
        const submitButton = document.getElementById('submitButton');
        const nextButton = document.getElementById('nextButton');

        // Enable or disable buttons based on input
        if (hasInput) {
            submitButton.disabled = false;
            nextButton.disabled = false;
        } else {
            submitButton.disabled = true;
            nextButton.disabled = true;
        }
    }

    // Add event listeners to input fields
    document.querySelectorAll('.input-container input').forEach(input => {
        input.addEventListener('input', checkInputs);
    });
    */

    function nextQuestion() {
        if (canProceed && (currentIndex < questionCount - 1)) {
            prevIndex = currentIndex
            currentIndex++;
            displayQuestion();
        }
    }

    function prevQuestion() {
        if (currentIndex > 0) {
            prevIndex = currentIndex
            currentIndex--;
            displayQuestion();
        }
    }

    function submitPressed() {
        if (canProceed) {
            alert('Form submitted!');
        }
    }
</script>
