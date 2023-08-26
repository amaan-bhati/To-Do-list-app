# To-do-list-app
Simple to do list app using HTML , CSS and Javascript



The To-Do List App is a practical web application that allows users to create, manage, and organize their tasks. Built with HTML, CSS, and JavaScript, this app offers a user-friendly interface for adding, completing, and removing tasks. The project is responsive and adaptable to various screen sizes.

Features
Add tasks to the to-do list.
Mark tasks as completed.
Remove tasks from the list.
Responsive design for seamless use on different devices.
Getting Started
Follow these steps to set up and run the To-Do List App on your local machine.

Prerequisites
Make sure you have a modern web browser that supports HTML5, CSS3, and JavaScript.

JavaScript Logic
The JavaScript code for the To-Do List App manages the tasks' state and interactions:

// Get references to HTML elements
const taskInput = document.getElementById('task-input');
const taskList = document.getElementById('task-list');

// Event listener for adding tasks
taskInput.addEventListener('keydown', (event) => {
  if (event.key === 'Enter' && taskInput.value.trim() !== '') {
    const taskText = taskInput.value.trim();
    addTask(taskText);
    taskInput.value = '';
  }
});

// Function to add a new task
function addTask(taskText) {
  const taskItem = document.createElement('li');
  taskItem.innerHTML = `
    <span class="task">${taskText}</span>
    <span class="delete">Delete</span>
  `;

  taskItem.querySelector('.delete').addEventListener('click', () => {
    taskItem.remove();
  });

  taskItem.querySelector('.task').addEventListener('click', () => {
    taskItem.classList.toggle('completed');
  });

  taskList.appendChild(taskItem);
}



Responsive Design
The To-Do List App is designed to be responsive, ensuring a seamless experience on various devices. This is achieved through CSS media queries that adjust the layout and styling to accommodate different screen sizes.

