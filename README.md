# Ex03 To-Do List using JavaScript
## Date:

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="todo-app">
        <h2>To-Do List 📝</h2>
        
        <div class="input-container">
            <input type="text" id="task-input" placeholder="Add a new task...">
            <button id="add-btn">Add Task</button>
        </div>

        <ul id="task-list"></ul>
    </div>

    <script src="script.js"></script>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background-color: #0f172a;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.todo-app {
    background-color: #1e293b;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
    width: 350px;
    color: #fff;
}

.todo-app h2 {
    margin-bottom: 20px;
    text-align: center;
}

.input-container {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
}

#task-input {
    flex: 1;
    padding: 10px;
    border: none;
    border-radius: 6px;
    outline: none;
}

#add-btn {
    background-color: #38bdf8;
    color: #0f172a;
    border: none;
    padding: 10px 15px;
    border-radius: 6px;
    font-weight: bold;
    cursor: pointer;
    transition: background 0.3s;
}

#add-btn:hover {
    background-color: #0284c7;
    color: #fff;
}

ul {
    list-style: none;
}

li {
    background-color: #334155;
    padding: 12px;
    margin-bottom: 10px;
    border-radius: 6px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: background 0.3s;
}

li.completed {
    text-decoration: line-through;
    opacity: 0.6;
}

.delete-btn {
    background-color: #ef4444;
    color: #fff;
    border: none;
    padding: 5px 10px;
    border-radius: 4px;
    cursor: pointer;
    font-size: 12px;
}

.delete-btn:hover {
    background-color: #dc2626;
}
const taskInput = document.getElementById("task-input");
const addBtn = document.getElementById("add-btn");
const taskList = document.getElementById("task-list");

addBtn.addEventListener("click", addTask);

function addTask() {
    const taskText = taskInput.value.trim();

    if (taskText === "") {
        alert("Please enter a task!");
        return;
    }

    const li = document.createElement("li");

    const span = document.createElement("span");
    span.textContent = taskText;
    span.addEventListener("click", function () {
        li.classList.toggle("completed");
    });

    const deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.classList.add("delete-btn");
    deleteBtn.addEventListener("click", function () {
        taskList.removeChild(li);
    });

    li.appendChild(span);
    li.appendChild(deleteBtn);
    taskList.appendChild(li);

    taskInput.value = "";
}


## OUTPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/787b578f-5daf-46a8-aef1-3968c7603c56" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
