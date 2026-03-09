Located in this repository is the Bug Crushers assignment for Multimedia Authoring. In it, we were
required to build a human anatomy puzzle and then identify two bugs in the system. The first was
creating code that would only allow one label to be dropped into a drop zone, as well as create
a reset button. To create the reset button, here is the code below that I used in JavaScript:
function dropped(e) {
    e.preventDefault();
    console.log("dropped");

    //prevent double drops here
    //if this dropzone has a child, don't let it drop
    //use a return statement

    if(this.firstElementChild) {
        return;
    }
    //drop the piece
    this.appendChild(currentDraggedElement);

    //reset the reference
    currentDraggedElement = null;
}
The second was to create a reset button using code. Here's the code I used in JavaScript:

resetbtn.addEventListener("click", function handleClick() {
    window.location.reload();
});

And in HTML:

<button class="resetbtn" id="resetbtn">Reset Puzzle</button>
