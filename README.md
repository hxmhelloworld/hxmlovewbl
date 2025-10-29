<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>王蓓灵，我喜欢你！</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            padding: 40px;
            text-align: center;
            max-width: 500px;
            width: 90%;
            position: relative;
            margin: 20px 0;
            max-height: 90vh;
            overflow-y: auto;
        }
        
        .heart {
            position: absolute;
            font-size: 20px;
            color: #ff4d6d;
            animation: float 5s infinite ease-in-out;
            opacity: 0.7;
            z-index: 1;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(20deg); }
        }
        
        h1 {
            color: #ff4d6d;
            margin-bottom: 20px;
            font-size: 28px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 2;
        }
        
        p {
            color: #555;
            margin-bottom: 30px;
            font-size: 18px;
            line-height: 1.6;
            position: relative;
            z-index: 2;
        }
        
        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
            position: relative;
            z-index: 2;
        }
        
        button {
            border: none;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 2;
        }
        
        #yesBtn {
            background: linear-gradient(to right, #ff4d6d, #ff8fa3);
            color: white;
            padding: 15px 30px;
            font-size: 18px;
            min-width: 120px;
        }
        
        #noBtn {
            background: linear-gradient(to right, #6c757d, #adb5bd);
            color: white;
            padding: 15px 30px;
            font-size: 18px;
            min-width: 120px;
            transition: all 0.5s ease;
        }
        
        #yesBtn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 77, 109, 0.3);
        }
        
        .success-message {
            display: none;
            margin-top: 30px;
            padding: 20px;
            background: linear-gradient(to right, #56ab2f, #a8e063);
            border-radius: 15px;
            color: white;
            font-size: 22px;
            font-weight: bold;
            animation: pulse 1.5s infinite;
            position: relative;
            z-index: 2;
        }
        
        .instructions {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 10px;
            color: #495057;
            font-size: 16px;
            text-align: left;
            position: relative;
            z-index: 2;
        }
        
        .instructions ol {
            padding-left: 20px;
            margin-top: 10px;
        }
        
        .instructions li {
            margin-bottom: 8px;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .hearts-container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
        }
        
        .copy-text {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 15px;
            background: #ff4d6d;
            color: white;
            border-radius: 20px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s ease;
        }
        
        .copy-text:hover {
            background: #e0445e;
        }
        
        .close-page {
            display: inline-block;
            margin-top: 15px;
            padding: 10px 20px;
            background: #6c757d;
            color: white;
            border-radius: 20px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s ease;
            border: none;
        }
        
        .close-page:hover {
            background: #5a6268;
        }
        
        /* 响应式设计 */
        @media (max-width: 480px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            p {
                font-size: 16px;
            }
            
            .buttons {
                flex-direction: column;
                align-items: center;
            }
            
            button {
                width: 100%;
                max-width: 200px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hearts-container" id="heartsContainer"></div>
        
        <h1>💖 王蓓灵，我喜欢你！ 💖</h1>
        <p>从遇见你的那一刻起，我的世界仿佛被点亮了一盏明灯。你的笑容如春日暖阳，温暖了我曾经平淡的生活；你的声音如清泉流淌，滋润了我干涸的心田。每一次与你相遇，都让我心跳加速；每一次与你交谈，都让我感到无比幸福。你是我生命中最美好的意外，是我愿意用一生去珍惜的缘分。你愿意成为我的女朋友，与我一起书写属于我们的故事吗？</p>
        
        <div class="buttons">
            <button id="yesBtn">同 意</button>
            <button id="noBtn">不同意</button>
        </div>
        
        <div class="success-message" id="successMessage">
            恭喜你成为华先猛女朋友！💕
        </div>
        
        <div class="instructions" id="instructions">
            <p>先复制表白文字</p>
            <ol>
                <li>点击下方"复制表白文字"按钮</li>
                <li>打开微信找到备注为"华先猛"的联系人</li>
                <li>粘贴发送"华先猛，我同意做你女朋友！"</li>
                <li>点击下方的"关闭本网页"按钮关闭此页面</li>
            </ol>
            <div style="text-align: center; margin-top: 15px;">
                <div class="copy-text" id="copyText">复制表白文字</div>
                <button class="close-page" id="closePage">关闭本网页</button>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const yesBtn = document.getElementById('yesBtn');
            const noBtn = document.getElementById('noBtn');
            const successMessage = document.getElementById('successMessage');
            const instructions = document.getElementById('instructions');
            const heartsContainer = document.getElementById('heartsContainer');
            const closePageBtn = document.getElementById('closePage');
            const copyTextBtn = document.getElementById('copyText');
            let noCount = 0;
            
            // 创建漂浮的爱心
            function createHearts() {
                for (let i = 0; i < 15; i++) {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    heart.innerHTML = '❤';
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.top = Math.random() * 100 + '%';
                    heart.style.animationDelay = Math.random() * 5 + 's';
                    heartsContainer.appendChild(heart);
                }
            }
            
            createHearts();
            
            // 复制文本到剪贴板
            copyTextBtn.addEventListener('click', function() {
                const textToCopy = "华先猛，我同意做你女朋友！";
                navigator.clipboard.writeText(textToCopy).then(() => {
                    copyTextBtn.textContent = "已复制!";
                    setTimeout(() => {
                        copyTextBtn.textContent = "复制表白文字";
                    }, 2000);
                }).catch(err => {
                    console.error('无法复制文本: ', err);
                    // 备用方案
                    const textArea = document.createElement('textarea');
                    textArea.value = textToCopy;
                    document.body.appendChild(textArea);
                    textArea.select();
                    document.execCommand('copy');
                    document.body.removeChild(textArea);
                    copyTextBtn.textContent = "已复制!";
                    setTimeout(() => {
                        copyTextBtn.textContent = "复制表白文字";
                    }, 2000);
                });
            });
            
            // 关闭网页
            closePageBtn.addEventListener('click', function() {
                if (confirm("确定要关闭这个页面吗？")) {
                    window.close();
                }
            });
            
            // 同意按钮点击事件
            yesBtn.addEventListener('click', function() {
                successMessage.style.display = 'block';
                instructions.style.display = 'block';
                yesBtn.style.display = 'none';
                noBtn.style.display = 'none';
                
                // 创建更多爱心动画
                for (let i = 0; i < 30; i++) {
                    setTimeout(() => {
                        const heart = document.createElement('div');
                        heart.classList.add('heart');
                        heart.innerHTML = '❤';
                        heart.style.left = Math.random() * 100 + '%';
                        heart.style.top = Math.random() * 100 + '%';
                        heart.style.animationDelay = Math.random() * 3 + 's';
                        heartsContainer.appendChild(heart);
                    }, i * 100);
                }
            });
            
            // 不同意按钮点击事件 - 添加挽留效果
            noBtn.addEventListener('click', function() {
                noCount++;
                
                // 更改"不同意"按钮的文字
                const messages = ["不同意", "真的不再想想?", "给个机会嘛", "最后考虑一下?", "确定要拒绝吗?"];
                if (noCount < messages.length) {
                    noBtn.textContent = messages[noCount];
                }
                
                // 缩小不同意按钮（整体尺寸）
                const scale = 1 - (noCount * 0.15); // 每次点击缩小15%
                
                if (scale > 0.3) { // 设置最小尺寸限制
                    noBtn.style.transform = `scale(${scale})`;
                    
                    // 放大同意按钮
                    const yesScale = 1 + (noCount * 0.2); // 每次点击放大20%
                    yesBtn.style.transform = `scale(${yesScale})`;
                    
                    // 移动不同意按钮
                    const moveX = Math.random() * 100 - 50;
                    const moveY = Math.random() * 100 - 50;
                    noBtn.style.transform = `scale(${scale}) translate(${moveX}px, ${moveY}px)`;
                }
                
                // 5次点击后隐藏不同意按钮并更改同意按钮文字
                if (noCount >= 5) {
                    noBtn.style.display = 'none';
                    yesBtn.textContent = "谢谢你的接受 ❤";
                }
            });
        });
    </script>
</body>
</html>
