<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple To-Do App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .app {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      width: 300px;
    }
    h2 {
      text-align: center;
    }
    input {
      width: 80%;
      padding: 8px;
      border: 1px solid #ddd;
      border-radius: 6px;
    }
    button {
      padding: 8px;
      margin-left: 5px;
      border: none;
      background: #4CAF50;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }
    ul {
      margin-top: 15px;
      padding: 0;
      list-style: none;
    }
    li {
      padding: 6px 0;
      border-bottom: 1px solid #eee;
    }
  </style>
</head>
<body>
  <div class="app">
    <h2>To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Enter a task...">
    <button onclick="addTask()">Add</button>
    <ul id="taskList"></ul>
  </div>

  <script>
    function addTask() {
      const input = document.getElementById("taskInput");
      const task = input.value.trim();
      if (task) {
        const li = document.createElement("li");
        li.textContent = task;
        document.getElementById("taskList").appendChild(li);
        input.value = "";
      }
    }
  </script>
</body>
</html>
