<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sự Kiện Roblox 2026</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:Segoe UI,sans-serif;
    background:linear-gradient(135deg,#00b4db,#0083b0);
    color:white;
}

.container{
    text-align:center;
    background:rgba(255,255,255,0.1);
    padding:35px;
    border-radius:20px;
    width:85%;
    max-width:420px;
    backdrop-filter:blur(10px);
    box-shadow:0 10px 30px rgba(0,0,0,0.3);
}

#main-title { transition: 0.3s; font-size: 22px; }

button{
    padding:15px 28px;
    font-size:20px;
    font-weight:bold;
    border:3px solid #00ff66;
    border-radius:12px;
    background:transparent;
    color:#00ff66;
    cursor:pointer;
    transition:.25s;
}

button:hover{
    background:#00ff66;
    color:black;
    box-shadow:0 0 15px #00ff66;
}

/* Loading Box chính */
#loading-box { display: none; margin-top: 20px; }
.spinner {
    width: 50px;
    height: 50px;
    border: 5px solid rgba(255,255,255,0.3);
    border-top: 5px solid #00ff66;
    border-radius: 50%;
    animation: spin 1s linear infinite;
    margin: 0 auto 15px;
}
#percent { font-size: 24px; font-weight: bold; color: #00ff66; }

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* reCAPTCHA Fake */
#captcha-container {
    display: none;
    background: #f9f9f9;
    border: 1px solid #d3d3d3;
    border-radius: 3px;
    width: 300px;
    height: 74px;
    margin: 20px auto;
    padding: 0 10px;
    color: #000;
    text-align: left;
}

.captcha-flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
}

.captcha-left { display: flex; align-items: center; }

#checkbox {
    width: 26px;
    height: 26px;
    border: 2px solid #c1c1c1;
    border-radius: 2px;
    background: #fff;
    cursor: pointer;
    margin-right: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
}

.mini-spinner {
    width: 22px;
    height: 22px;
    border: 3px solid #4d90fe;
    border-top: 3px solid transparent;
    border-radius: 50%;
    animation: spin 0.8s linear infinite;
    box-sizing: border-box;
}

#checkbox.loading {
    border: none;
    background: transparent;
}

.captcha-text { font-size: 14px; font-weight: 400; font-family: Roboto, Arial, sans-serif; }
.captcha-right { text-align: center; font-size: 10px; color: #555; }
.captcha-right img { width: 28px; }

/* QR Box - Vuông góc hoàn toàn, ko bo tròn */
#qr-box{
    display:none;
    margin:20px auto 0;
    width:200px;
    height:200px;
    overflow:hidden;
    animation:show .4s ease;
    /* Đảm bảo ko có bo góc ở đây */
    border-radius: 0 !important; 
}

#qr-box img{ 
    width:100%; 
    height:100%; 
    /* Triệt tiêu mọi thuộc tính bo góc */
    border-radius: 0 !important; 
}

.msg{
    display:none;
    margin-top:15px;
    color:white;
    font-weight:bold;
    font-size: 16px;
}

@keyframes show{ from{ opacity:0; transform:scale(.8); } to{ opacity:1; transform:scale(1); } }
</style>
</head>

<body>

<div class="container">
    <h1 id="main-title">SỰ KIỆN ROBLOX</h1>
    <p id="sub-text">Chúc mừng! Bạn đủ điều kiện nhận 1000 Robux.</p>

    <button id="btn" onclick="startLoading()">Nhận 1000 Robux!</button>

    <div id="loading-box">
        <div class="spinner"></div>
        <div id="percent">0%</div>
        <p>Đang kiểm tra thông tin...</p>
    </div>

    <div id="captcha-container">
        <div class="captcha-flex">
            <div class="captcha-left">
                <div id="checkbox" onclick="verifyCaptcha()"></div>
                <div class="captcha-text">Tôi dell phải là robot</div>
            </div>
            <div class="captcha-right">
                <img src="https://www.gstatic.com/recaptcha/api2/logo_48.png" alt="reCAPTCHA">
                <div style="margin-top:2px;">reCAPTCHA</div>
                <div style="font-size:8px;">Bảo mật - Điều khoản</div>
            </div>
        </div>
    </div>

    <div id="qr-box">
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://www.youtube.com/watch?v=dQw4w9WgXcQ">
    </div>

    <div id="msg" class="msg">Quét QR ngay để nhận thưởng!</div>
</div>

<script>
function startLoading() {
    const btn = document.getElementById("btn");
    const loadingBox = document.getElementById("loading-box");
    const percentTxt = document.getElementById("percent");
    const subText = document.getElementById("sub-text");

    btn.style.display = "none";
    subText.style.display = "none";
    loadingBox.style.display = "block";

    percentTxt.innerText = "1%";

    setTimeout(() => {
        percentTxt.innerText = "42%";
        setTimeout(() => {
            percentTxt.innerText = "62%";
            setTimeout(() => {
                percentTxt.innerText = "82%";
                setTimeout(() => {
                    percentTxt.innerText = "99%";
                    setTimeout(() => {
                        percentTxt.innerText = "100%";
                        setTimeout(() => {
                            loadingBox.style.display = "none";
                            document.getElementById("main-title").innerText = "Khoan đã, bạn có phải robot không?";
                            document.getElementById("captcha-container").style.display = "block";
                        }, 500);
                    }, 3000);
                }, 200);
            }, 700);
        }, 1000);
    }, 500);
}

function verifyCaptcha() {
    const checkbox = document.getElementById("checkbox");
    checkbox.innerHTML = '<div class="mini-spinner"></div>';
    checkbox.classList.add("loading");
    checkbox.onclick = null;

    setTimeout(() => {
        document.getElementById("captcha-container").style.display = "none";
        document.getElementById("main-title").innerText = "CHÚC MỪNG!";
        document.getElementById("main-title").style.color = "#00ff66";
        document.getElementById("qr-box").style.display = "block";
        document.getElementById("msg").style.display = "block";
    }, 5000);
}
</script>

</body>
</html>
