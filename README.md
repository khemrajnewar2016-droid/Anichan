# Anichan
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Anisha, will you be my Valentine?</title>
<style>
    body{
        margin:0;
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        background:#ffe6f0;
        font-family: Arial, Helvetica, sans-serif;
        overflow:hidden;
        text-align:center;
    }
    .card{
        background:white;
        padding:30px 20px;
        border-radius:20px;
        box-shadow:0 10px 30px rgba(0,0,0,0.1);
        width:90%;
        max-width:350px;
        position:relative;
    }
    h1{
        color:#ff4d88;
        font-size:22px;
    }
    p{
        font-size:16px;
        color:#444;
    }
    .buttons{
        margin-top:25px;
        position:relative;
        height:120px;
    }
    button{
        padding:12px 20px;
        border:none;
        border-radius:25px;
        font-size:16px;
        cursor:pointer;
        position:absolute;
        transition:0.2s;
    }
    #yes{
        background:#ff4d88;
        color:white;
        left:20%;
    }
    #no{
        background:#ddd;
        color:#333;
        right:20%;
    }
    .message{
        margin-top:20px;
        font-size:18px;
        color:#ff4d88;
        display:none;
    }
</style>
</head>
<body>

<div class="card">
    <h1>Anisha, will you be my Valentine? 💖</h1>
    <p>You can think carefully before answering…<br>
    but there is a tiny problem 😌</p>

    <div class="buttons">
        <button id="yes">Yes, of course 💘</button>
        <button id="no">No</button>
    </div>

    <div class="message" id="msg">
        I knew it! See you on Valentine’s, Anisha ❤️
    </div>
</div>

<script>
const noBtn = document.getElementById('no');
const yesBtn = document.getElementById('yes');
const msg = document.getElementById('msg');

noBtn.addEventListener('touchstart', moveButton);
noBtn.addEventListener('mouseover', moveButton);

function moveButton(){
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.position = "fixed";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

yesBtn.addEventListener('click', () => {
    msg.style.display = "block";
});
</script>

</body>
</html>