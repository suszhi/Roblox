<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>六 · 七 | 简单数字美学</title>
    <!-- 极简风格，只保留清晰的设计与 subtle 的67元素 -->
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #f2f5f9;
            font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            color: #1b2e35;
            line-height: 1.5;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* 柔和容器 */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem 2rem;
            width: 100%;
        }

        /* 标头 — 纯粹 67 */
        .site-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 2rem;
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(6px);
            -webkit-backdrop-filter: blur(6px);
            border-bottom: 2px solid rgba(55, 90, 100, 0.1);
        }

        .logo-67 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: -2px;
            background: linear-gradient(150deg, #1d4b5e, #3f7b6e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo-67 span {
            background: none;
            font-weight: 800;
            font-size: 2.5rem;
            -webkit-text-fill-color: #2f6b62;
        }

        .nav-mini {
            display: flex;
            gap: 2rem;
            font-weight: 500;
            color: #2f5850;
        }
        .nav-mini a {
            text-decoration: none;
            color: inherit;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
        }
        .nav-mini a:hover {
            border-bottom-color: #519e8c;
        }

        /* 主数字 67 面板 */
        .hero-67 {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 2rem 1rem 1rem 1rem;
        }

        .big-67 {
            font-size: 16vw;
            font-weight: 800;
            line-height: 1;
            background: linear-gradient(145deg, #1d5b4f, #305f6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.05em;
            filter: drop-shadow(0 4px 12px #214d4a33);
            margin-bottom: 0.5rem;
        }

        .sub-digit {
            font-size: 1.5rem;
            font-weight: 400;
            color: #568f86;
            letter-spacing: 8px;
            text-transform: uppercase;
            margin-top: -1rem;
        }

        .legend {
            max-width: 580px;
            margin: 1.8rem auto;
            background: #ffffffbc;
            backdrop-filter: blur(4px);
            border-radius: 120px;
            padding: 0.9rem 1.8rem;
            border: 1px solid #c7e0d7;
            color: #1c4845;
            font-weight: 500;
            box-shadow: 0 6px 14px #d7eae3;
            text-align: center;
        }

        /* 卡片——展示两个数字的魅力 6 与 7 分开 */
        .double-card {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin: 4rem 0 2rem 0;
            justify-content: center;
        }

        .card-six, .card-seven {
            flex: 1 1 200px;
            background: #ffffffdd;
            backdrop-filter: blur(3px);
            padding: 2.5rem 1.8rem;
            border-radius: 48px;
            box-shadow: 0 25px 35px -22px #194d47;
            border: 1px solid #b4dfd1;
            transition: 0.25s;
            text-align: center;
        }

        .card-six:hover, .card-seven:hover {
            transform: scale(1.02) translateY(-6px);
            border-color: #519e8c;
        }

        .digit-icon {
            font-size: 5rem;
            font-weight: 800;
            line-height: 1;
            background: linear-gradient(130deg, #1d5f51, #257d68);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.8rem;
        }

        .card-six h3, .card-seven h3 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            color: #1f4c47;
        }

        .card-six p, .card-seven p {
            color: #386f64;
        }

        /* 分隔线 67 小元素 */
        .rule-67 {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.6rem;
            margin: 2rem 0;
        }
        .rule-67 .line {
            height: 3px;
            width: 50px;
            background: linear-gradient(90deg, #6bb2a0, #367a6b);
            border-radius: 6px;
        }
        .rule-67 span {
            font-size: 2rem;
            font-weight: 600;
            color: #589e8d;
        }

        /* 细信息 — 67 的平方 / 趣味 */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.2rem;
            margin: 3rem 0;
        }

        .info-item {
            background: #ebf6f1;
            border-radius: 36px;
            padding: 1.6rem 0.8rem;
            text-align: center;
            border: 1px solid #bbe6da;
            box-shadow: inset 0 -2px 0 #bedbd0;
        }

        .info-item .number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(145deg, #30655b, #154b49);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .info-item .label {
            color: #36776a;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* 页脚 67 签名 */
        .footer-67 {
            margin-top: 3.5rem;
            background: #d2eee4;
            border-radius: 60px 60px 0 0;
            padding: 2rem 2rem 1.5rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            color: #175249;
        }

        .footer-67 .copy {
            font-size: 1.2rem;
            font-weight: 500;
        }

        .stamp-67 {
            display: flex;
            align-items: center;
            gap: 10px;
            background: #ffffff7c;
            padding: 0.5rem 1.5rem;
            border-radius: 60px;
            font-weight: 600;
            border: 2px solid #2f7768;
        }

        /* 响应式 */
        @media (max-width: 600px) {
            .big-67 { font-size: 30vw; }
            .info-grid { grid-template-columns: 1fr; }
            .double-card { flex-direction: column; }
            .site-header { flex-direction: column; gap: 0.5rem; }
        }

        /* 纯数字装饰线 */
        .tiny-67 {
            color: #64aa99;
            font-weight: 300;
            font-size: 1rem;
            margin-top: 2rem;
            text-align: center;
        }
        hr {
            border: 1px solid #bae1d4;
            width: 80%;
            margin: 1rem auto;
        }
    </style>
</head>
<body>

<!-- 非常简单的头部，只有67和导航符号 -->
<header class="site-header">
    <div class="logo-67">
        <span>6</span>7 <span style="font-size: 1.2rem; -webkit-text-fill-color: #4d897b;">//</span>
    </div>
    <div class="nav-mini">
        <a href="#">六</a>
        <a href="#">七</a>
        <a href="#">67合</a>
        <a href="#">核</a>
    </div>
</header>

<main class="container">
    <!-- 巨型 67 视觉焦点 -->
    <div class="hero-67">
        <div class="big-67">67</div>
        <div class="sub-digit">SIX  ·  SEVEN</div>
        <div class="legend">
            ⚡ 纯粹的数字美学 — 67 只是两个数字，但不止两个数字。
        </div>
    </div>

    <!-- 6 与 7 两个独立块 简单阐释 -->
    <div class="double-card">
        <div class="card-six">
            <div class="digit-icon">6</div>
            <h3>六 · 顺</h3>
            <p>平衡 · 流畅 · 六边形之力。代表安稳与结构的数字，在东方寓意顺遂。</p>
        </div>
        <div class="card-seven">
            <div class="digit-icon">7</div>
            <h3>七 · 启</h3>
            <p>幸运 · 探索 · 七和弦。一周七天，彩虹七色，充满可能性的数字。</p>
        </div>
    </div>

    <!-- 67 装饰线 -->
    <div class="rule-67">
        <span class="line"></span>
        <span>✦ 67 ✦</span>
        <span class="line"></span>
    </div>

    <!-- 关于 67 的趣味数据 (极简主义格子) -->
    <div class="info-grid">
        <div class="info-item">
            <div class="number">6+7</div>
            <div class="label">和 · 十三</div>
        </div>
        <div class="info-item">
            <div class="number">6×7</div>
            <div class="label">积 · 四十二</div>
        </div>
        <div class="info-item">
            <div class="number">67²</div>
            <div class="label">平方 · 4489</div>
        </div>
    </div>

    <!-- 一段简洁文字，解释67网站的意义 -->
    <div style="background: #f5fdf9; border-radius: 50px; padding: 2rem; margin: 2rem 0; border: 1px solid #bbebdb;">
        <p style="font-size: 1.2rem; color: #1d5a50;  font-weight: 400;">
            <span style="font-size: 2rem; font-weight: 600; margin-right: 0.8rem;">67</span> 
            是一个简洁的数字组合。这个网站只为展示 67 而存在 —— 
            没有多余的动效，没有臃肿的图片，只有数字本身以及围绕它的一点点遐想。
            你可以把 67 看作一个坐标、一个代号或者一个随机的灵感。
        </p>
    </div>

    <!-- 微小的收尾 67 -->
    <div style="text-align: right; font-size: 3rem; opacity: 0.15; font-weight: 800; user-select: none;">67</div>
    <hr>
    <div class="tiny-67">
        ❖ 一个非常简单的 67 品牌站点 ❖
    </div>
</main>

<!-- 页脚部分 67 无处不在 -->
<footer class="footer-67">
    <div class="copy">
        © 2026 六 · 七 简单数字
    </div>
    <div class="stamp-67">
        <span>6</span>|<span>7</span>
        <i class="no-icon" style="font-weight: 200;">#</i>
    </div>
    <div style="display: flex; gap: 20px;">
        <span>6:7</span>
        <span>67%</span>
    </div>
</footer>

<!-- 没有任何复杂 js，只有一行控制台彩蛋（可选） -->
<script>
    // 纯静的控制台问候 —— 67 精神
    console.log('%c 67 %c 简单即永恒 ', 'background: #1d5f51; color: #e2ffe8; font-size: 20px; padding: 6px 12px; border-radius: 30px;', 'background: #d1efe3; color: #174e40; font-size: 16px; padding: 6px 12px; border-radius: 30px;');
    // 可以忽略，只是装饰
</script>
</body>
</html>