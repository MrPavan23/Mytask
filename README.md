<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            position: relative;
            min-height: 100vh;
            background-color: #ffffff;
        }

        .task-bar {
            background-color: #ffffff;
            color: #ffffff;
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            transition: background-color 0.3s;
        }

        .bottom-task-bar {
            background-color: #ffffff;
            color: #ffffff;
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            transition: background-color 0.3s;
        }

        .task-bar-icons {
            display: flex;
        }

        .task-bar-icons a {
            color: #000000;
            text-decoration: none;
            margin-left: 10px;
        }

        .big-text {
            margin-left: 10px;
            font-size: 20px;
            margin-top: 60px;
            display: flex;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .star-icon {
            width: 20px;
            height: 20px;
        }

        .label {
            font-size: 10px;
            background-color: #f2f2f2;
            padding: 2px 5px;
            border-radius: 3px;
            position: absolute;
            bottom: 4px;
            left: 50%;
            transform: translateX(-50%);
        }
    </style>
</head>
<body>
<div class="task-bar" id="top-taskbar">
    <div class="task-bar-icons">
        <a href="#"><img alt="Left Arrow" src="left-arrow-icon.png" width="20" height="20"></a>
    </div>
    <div class="task-bar-icons">
        <a href="#"><img src="archive-icon.png" alt="Archive Symbol" style="width: 20px; margin-right: 10px;"></a>
        <a href="#"><img src="delete-icon.png" alt="Delete Symbol" width="17" height="18" style="margin-right: 10px;"></a>
        <a href="#"><img src="unread-icon.png" alt="Draft Symbol" width="25" height="23" style="width: 20px; margin-right: 10px;"></a>
        <a href="#"><img src="dot-icon.png" alt="Dots Symbol" width="20" height="20" style="width: 20px; margin-right: 10px;"></a>
    </div>
</div>

<div class="big-text">
    <span>Request for Early Departure on Every Wednesday for WIN SEM 2023-2024</span>
    <span class="label">Inbox</span>
    <img src="star-icon.png" alt="Star Icon" class="star-icon">
</div>

<div class="bottom-task-bar" id="bottom-taskbar">
    <div class="task-bar-icons">
        <a href="#">Icon 1</a>
        <a href="#">Icon 2</a>
        <a href="#">Icon 3</a>
    </div>
</div>

<script>
    window.onscroll = function() {scrollFunction()};

    function scrollFunction() {
        var footer = document.getElementById("thanks-footer");
        if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
            document.getElementById("top-taskbar").style.backgroundColor = "#f2f2f2";
            document.getElementById("bottom-taskbar").style.backgroundColor = "#f2f2f2";
        } else {
            document.getElementById("top-taskbar").style.backgroundColor = "#ffffff";
            document.getElementById("bottom-taskbar").style.backgroundColor = "#f2f2f2";
        }
    }
</script>

</body>
</html>
