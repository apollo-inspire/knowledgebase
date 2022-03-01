
```js
window.addEventListener('load', init);
//Global variables
let imageList = ['ballonnen', 'cars', 'planes', 'goudkistje'];
let playingField;
/**
 * Initialize after the DOM is ready
 */
function init() {
    playingField = document.getElementById(`playing-field`);
    console.log(playingField);
    createPlayField();
}
/**
 * Generate the playing field dynamically with all the available images
 */
function createPlayField() {
    playingField = document.getElementById(`playing-field`);
    shuffleArray(imageList);
    for (let image in imageList) {
        console.log(imageList[image])
        //create card
        let card = document.createElement("div");
        card.classList.add(`playing-card`);
        playingField.appendChild(card);
        //add number
        let num = document.createElement("h2");
        num.innerHTML = image;
        card.appendChild(num);
        //image add
        let img = document.createElement("img");
        img.src = `./img/${imageList[image]}.png`
        card.appendChild(img);
    }
}
/**
 * Show the card by its front so the player knows whats going on
 *
 * @param e
 */
function playingFieldClickHandler(e) {
}
/**
 * Handler for when the form is submitted
 *
 * @param e
 */
function formSubmitHandler(e) {
}
/**
 * Write text for the user as feedback of their answer
 *
 * @param text
 */
function writeFeedbackMessage(text) {
}
/**
 * Randomize array element order in-place.
 * Using Durstenfeld shuffle algorithm.
 * @link http://stackoverflow.com/a/12646864
 *
 * @param array
 * @returns {*}
 */
function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
        let j = Math.floor(Math.random() * (i + 1));
        let temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }
    return array;
}
```