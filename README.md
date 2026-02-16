<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Подтверждение сертификата</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f3f4f6;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    text-align: center;
}

.logo {
    width: 90px;
    margin-bottom: 15px;
}

.title {
    font-size: 15px;
    color: #333;
    margin-bottom: 25px;
}

.card {
    background: white;
    padding: 25px;
    width: 320px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

.label {
    text-align: left;
    font-size: 14px;
    margin-bottom: 5px;
}

input {
    width: 100%;
    padding: 10px;
    border: 1px solid #d1d5db;
    border-radius: 5px;
    margin-bottom: 12px;
    font-size: 14px;
}

button {
    width: 100%;
    padding: 10px;
    background: #3b6edc;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 14px;
    cursor: pointer;
}

button:hover {
    background: #2f5bcc;
}

.error {
    color: red;
    font-size: 13px;
    margin-top: 8px;
}
</style>
</head>

<body>

<div class="container">
    <img class="logo" src="https://upload.wikimedia.org/wikipedia/commons/7/77/Emblem_of_Uzbekistan.svg">
    
    <div class="title">
        Министерство здравоохранения<br>
        Республики Узбекистан
    </div>

    <div class="card">
        <div class="label">Код подтверждения</div>
        <input type="password" id="code" maxlength="4" placeholder="Введите код">
        <button onclick="checkCode()">Подтвердить</button>
        <div id="error" class="error"></div>
    </div>
</div>

<script>
function checkCode() {
    var correctCode = "1234"; // ← здесь меняешь код
    var entered = document.getElementById("code").value;

    if (entered === correctCode) {
        window.location.href = "file.pdf"; // ← сюда вставь свой PDF
    } else {
        document.getElementById("error").innerText = "Неверный код";
    }
}
</script>

</body>
</html>
