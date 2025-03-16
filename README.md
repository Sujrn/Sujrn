<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>서민 생활 정보 플랫폼</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>서민 생활 정보 플랫폼</h1>
        <nav>
            <ul>
                <li><a href="#discount-info">할인 정보</a></li>
                <li><a href="#support-program">지원 프로그램</a></li>
                <li><a href="#community">커뮤니티</a></li>
            </ul>
        </nav>
    </header>

    <section id="discount-info">
        <h2>저렴한 생활 정보</h2>
        <p>여기서 최신 할인 정보와 쇼핑 팁을 확인할 수 있습니다.</p>
        <ul id="discount-list">
            <!-- 할인 정보 목록이 동적으로 들어갈 곳 -->
        </ul>
    </section>

    <section id="support-program">
        <h2>공공 서비스 & 지원 프로그램</h2>
        <p>정부에서 제공하는 다양한 지원 프로그램 정보를 제공합니다.</p>
        <ul id="support-list">
            <!-- 지원 프로그램 목록 -->
        </ul>
    </section>

    <section id="community">
        <h2>커뮤니티</h2>
        <p>서민들이 정보와 경험을 공유하는 공간입니다.</p>
        <div id="community-discussion">
            <!-- 커뮤니티 게시판 기능 -->
        </div>
    </section>

    <footer>
        <p>&copy; 2025 서민 생활 정보 플랫폼</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

header nav ul {
    list-style: none;
    padding: 0;
}

header nav ul li {
    display: inline;
    margin: 0 15px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
}

section {
    padding: 20px;
    margin: 20px;
    background-color: white;
    border-radius: 8px;
}

h2 {
    color: #333;
}

ul {
    padding-left: 20px;
}

footer {
    text-align: center;
    padding: 20px;
    background-color: #333;
    color: white;
}
// script.js
document.addEventListener('DOMContentLoaded', function() {
    const discountInfo = [
        { title: "할인 이벤트 1", description: "10% 할인, 2월 28일까지" },
        { title: "할인 이벤트 2", description: "50% 할인, 특정 브랜드" },
        { title: "할인 이벤트 3", description: "새로운 고객 20% 할인" },
    ];

    const supportPrograms = [
        { title: "기초생활수급자 지원", description: "기초생활수급자를 위한 지원 프로그램" },
        { title: "청년 창업 지원", description: "청년 창업자를 위한 지원금과 혜택" },
        { title: "취업 지원 프로그램", description: "실업자와 구직자를 위한 취업 프로그램" },
    ];

    function displayDiscounts() {
        const list = document.getElementById("discount-list");
        discountInfo.forEach(info => {
            const listItem = document.createElement("li");
            listItem.textContent = `${info.title}: ${info.description}`;
            list.appendChild(listItem);
        });
    }

    function displaySupportPrograms() {
        const list = document.getElementById("support-list");
        supportPrograms.forEach(program => {
            const listItem = document.createElement("li");
            listItem.textContent = `${program.title}: ${program.description}`;
            list.appendChild(listItem);
        });
    }

    displayDiscounts();
    displaySupportPrograms();
});
