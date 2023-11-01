function addTask() {
    var task = document.getElementById("task").value;
    if (task === "") {
        alert("Task cannot be empty!");
    } else {
        var taskList = document.getElementById("taskList");
        var li = document.createElement("li");
        li.appendChild(document.createTextNode(task));
        taskList.appendChild(li);
        document.getElementById("task").value = "";

        // Optional: Add functionality to remove tasks
        li.onclick = function() {
            this.parentNode.removeChild(this);
        };
    }
}
