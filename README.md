<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>一站式进步平台</title>
    <style>
        /* ---- 全局变量 ---- */
        :root {
            --grad-1: #667eea;
            --grad-2: #764ba2;
            --glass: rgba(255, 255, 255, 0.25);
            --blur: 12px;
            --radius: 24px;
            --shadow: 0 8px 32px rgba(0, 0, 0, 0.15);
            --text: #2c3e50;
            --text-light: #7f8c8d;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, var(--grad-1) 0%, var(--grad-2) 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 40px 20px;
            color: var(--text);
        }

        .container {
            width: 100%;
            max-width: 1200px;
        }

        /* ---- 头部 ---- */
        .header {
            text-align: center;
            margin-bottom: 60px;
            animation: fadeInDown 0.8s ease;
        }

        .header h1 {
            font-size: 52px;
            font-weight: 700;
            letter-spacing: 2px;
            color: #fff;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
            margin-bottom: 10px;
        }

        .header p {
            font-size: 20px;
            color: rgba(255, 255, 255, 0.85);
        }

        /* ---- 网格 ---- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .service-category {
            background: var(--glass);
            backdrop-filter: blur(var(--blur));
            -webkit-backdrop-filter: blur(var(--blur));
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            border: 1px solid rgba(255, 255, 255, 0.18);
            padding: 32px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeInUp 1s ease both;
        }

        .service-category:nth-child(2) {
            animation-delay: 0.15s;
        }

        .service-category:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.2);
        }

        .category-header {
            display: flex;
            align-items: center;
            margin-bottom: 24px;
        }

        .category-icon {
            font-size: 48px;
            margin-right: 18px;
            filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.1));
        }

        .category-title {
            font-size: 28px;
            font-weight: 600;
            color: #fff;
            letter-spacing: 1px;
        }

        .service-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .service-item {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 16px;
            padding: 18px 24px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-item:hover {
            background: #fff;
            transform: translateX(6px);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        }

        .service-link {
            display: flex;
            justify-content: space-between;
            align-items: center;
            text-decoration: none;
            color: var(--text);
        }

        .service-name {
            font-weight: 600;
            font-size: 17px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .service-desc {
            font-size: 14px;
            color: var(--text-light);
            margin-top: 4px;
        }

        .service-status {
            font-size: 12px;
            font-weight: 600;
            padding: 5px 12px;
            border-radius: 20px;
            background: #e8f5e9;
            color: #2e7d32;
        }

        .external-link::after {
            content: "↗";
            font-size: 13px;
            margin-left: 4px;
            opacity: 0.7;
        }

        /* ---- 动画 ---- */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ---- 涟漪 ---- */
        @keyframes ripple {
            to {
                transform: scale(2.5);
                opacity: 0;
            }
        }

        /* ---- 响应式 ---- */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 40px;
            }
            .services-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1>🎯 一站式进步平台</h1>
            <p>林鸿鹤版本</p>
        </header>

        <main class="services-grid">
            <!-- 学习使用 -->
            <div class="service-category">
                <div class="category-header">
                    <div class="category-icon">🎓</div>
                    <h3 class="category-title">学习使用</h3>
                </div>
                <ul class="service-list">
                    <li class="service-item" onclick="window.open('https://kimi.moonshot.cn', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">Kimi AI助手</div>
                                <div class="service-desc">智能问答和学习辅助工具</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('https://www.doubao.com', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">豆包 AI助手</div>
                                <div class="service-desc">智能问答和学习辅助工具</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('https://www.runoob.com', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">菜鸟教程</div>
                                <div class="service-desc">编程学习</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('https://www.csdn.net', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">CSDN技术社区</div>
                                <div class="service-desc">编程学习和技术交流平台</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                </ul>
            </div>

            <!-- 进步之路 -->
            <div class="service-category">
                <div class="category-header">
                    <div class="category-icon">🏛️</div>
                    <h3 class="category-title">进步之路</h3>
                </div>
                <ul class="service-list">
                    <li class="service-item" onclick="window.open('http://bm.scs.gov.cn/kl2026', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">国家公务员考试</div>
                                <div class="service-desc">国考成绩查询入口</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('https://gwykl.fujian.gov.cn/portal', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">福建省级公务员考试</div>
                                <div class="service-desc">福建省省考成绩查询</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('http://ksbm.fjrst.cn:8903/home', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">福建事业编考试</div>
                                <div class="service-desc">福建事业单位招聘考试成绩</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                    <li class="service-item" onclick="window.open('https://yz.chsi.com.cn/cjcx/', '_blank')">
                        <div class="service-link">
                            <div>
                                <div class="service-name external-link">考研成绩查询</div>
                                <div class="service-desc">全国硕士研究生考试成绩</div>
                            </div>
                            <span class="service-status">跳转</span>
                        </div>
                    </li>
                </ul>
            </div>
        </main>
    </div>

    <script>
        // 涟漪动画
        document.querySelectorAll('.service-item').forEach(item => {
            item.addEventListener('click', function(e) {
                const ripple = document.createElement('span');
                const rect = this.getBoundingClientRect();
                const size = Math.max(rect.width, rect.height);
                const x = e.clientX - rect.left - size / 2;
                const y = e.clientY - rect.top - size / 2;
                ripple.style.cssText = `
                    position: absolute; width: ${size}px; height: ${size}px;
                    left: ${x}px; top: ${y}px;
                    background: rgba(102,126,234,0.25);
                    border-radius: 50%; transform: scale(0);
                    animation: ripple 0.6s linear; pointer-events: none;
                `;
                this.style.position = 'relative'; this.style.overflow = 'hidden';
                this.appendChild(ripple);
                setTimeout(() => ripple.remove(), 600);
            });
        });
    </script>
</body>
</html>
