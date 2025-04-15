<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>日历卡片生成工具</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
        }
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #f5f5f5;
            padding: 30px;
            min-height: 100vh;
        }
        .container {
            width: 100%;
            max-width: 1000px;
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
            color: #333;
        }
        .input-section {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #333;
        }
        textarea, input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        textarea {
            height: 120px;
            resize: vertical;
        }
        .button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #45a049;
        }
        .output-section {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .card-container {
            width: 100%;
            max-width: 400px;
            margin-bottom: 20px;
        }
        .calendar-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            position: relative;
        }
        .card-date {
            background-color: #3f51b5;
            color: white;
            padding: 15px;
            text-align: center;
        }
        .card-day {
            font-size: 36px;
            font-weight: bold;
            line-height: 1;
        }
        .card-month-year {
            font-size: 16px;
            margin-top: 5px;
        }
        .card-weekday {
            font-size: 18px;
            margin-top: 5px;
        }
        .card-content {
            padding: 20px;
            min-height: 150px;
        }
        .card-quote {
            font-size: 18px;
            line-height: 1.5;
            color: #333;
            margin-bottom: 15px;
        }
        .card-source {
            font-size: 14px;
            color: #666;
            text-align: right;
            font-style: italic;
        }
        .card-actions {
            margin-top: 20px;
            display: flex;
            justify-content: center;
        }
        .button-download {
            background-color: #2196F3;
        }
        .button-download:hover {
            background-color: #0b7dda;
        }
        .button-random {
            background-color: #9C27B0;
            margin-right: 10px;
        }
        .button-random:hover {
            background-color: #7B1FA2;
        }
        .form-actions {
            display: flex;
            justify-content: flex-end;
        }
        .hidden {
            display: none;
        }
        @media (max-width: 600px) {
            .container {
                gap: 20px;
            }
            .card-container {
                max-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>日历卡片生成工具</h1>
        
        <div class="input-section">
            <div class="form-group">
                <label for="content">文案内容:</label>
                <textarea id="content" placeholder="请输入文案内容..."></textarea>
            </div>
            <div class="form-group">
                <label for="source">来源:</label>
                <input type="text" id="source" placeholder="请输入来源...">
            </div>
            <div class="form-actions">
                <button id="random-btn" class="button button-random">随机</button>
                <button id="generate-btn" class="button">生成卡片</button>
            </div>
        </div>
        
        <div class="output-section">
            <div id="card-container" class="card-container hidden">
                <div id="calendar-card" class="calendar-card">
                    <div class="card-date">
                        <div class="card-day" id="day"></div>
                        <div class="card-month-year" id="month-year"></div>
                        <div class="card-weekday" id="weekday"></div>
                    </div>
                    <div class="card-content">
                        <div class="card-quote" id="quote"></div>
                        <div class="card-source" id="quote-source"></div>
                    </div>
                </div>
            </div>
            <div class="card-actions">
                <button id="download-btn" class="button button-download hidden">下载卡片</button>
            </div>
        </div>
    </div>

    <script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const generateBtn = document.getElementById('generate-btn');
            const downloadBtn = document.getElementById('download-btn');
            const cardContainer = document.getElementById('card-container');
            const calendarCard = document.getElementById('calendar-card');
            
            const dayElement = document.getElementById('day');
            const monthYearElement = document.getElementById('month-year');
            const weekdayElement = document.getElementById('weekday');
            const quoteElement = document.getElementById('quote');
            const sourceElement = document.getElementById('quote-source');
            
            const contentInput = document.getElementById('content');
            const sourceInput = document.getElementById('source');
            const randomBtn = document.getElementById('random-btn');
            
            // 格式化时间函数
            function formatDate() {
                const now = new Date();
                const day = now.getDate();
                
                const monthNames = ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月'];
                const month = monthNames[now.getMonth()];
                
                const year = now.getFullYear();
                
                const weekdayNames = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
                const weekday = weekdayNames[now.getDay()];
                
                return { day, month, year, weekday };
            }
            
            // 生成卡片
            generateBtn.addEventListener('click', () => {
                const content = contentInput.value.trim();
                const source = sourceInput.value.trim();
                
                if (!content) {
                    alert('请输入文案内容');
                    return;
                }
                
                const { day, month, year, weekday } = formatDate();
                
                dayElement.textContent = day;
                monthYearElement.textContent = `${month} ${year}`;
                weekdayElement.textContent = weekday;
                quoteElement.textContent = content;
                sourceElement.textContent = source ? `——${source}` : '';
                
                cardContainer.classList.remove('hidden');
                downloadBtn.classList.remove('hidden');
            });
            
            // 下载卡片
            downloadBtn.addEventListener('click', () => {
                html2canvas(calendarCard).then(canvas => {
                    const link = document.createElement('a');
                    link.download = `日历卡片_${new Date().toLocaleDateString().replace(/\//g, '-')}.png`;
                    link.href = canvas.toDataURL('image/png');
                    link.click();
                });
            });

            // 随机获取名言
            randomBtn.addEventListener('click', async () => {
                try {
                    // 显示加载状态
                    randomBtn.textContent = '加载中...';
                    randomBtn.disabled = true;
                    
                    const response = await fetch('https://api.siliconflow.cn/v1/chat/completions', {
                        method: 'POST',
                        headers: {
                            'Authorization': 'Bearer sk-hxmkrirwrhbeepcivtgwmhhxnszljdzxyunkybmjgjojeeig',
                            'Content-Type': 'application/json'
                        },
                        body: JSON.stringify({
                            "model": "Qwen/Qwen2.5-14B-Instruct",
                            "stream": false,
                            "max_tokens": 512,
                            "temperature": 0.7,
                            "top_p": 0.7,
                            "top_k": 50,
                            "frequency_penalty": 0.5,
                            "n": 1,
                            "stop": [],
                            "messages": [
                                {
                                "role": "user",
                                "content": "随机回复我一句金句及出处，包括不限于影视剧、名人名言、名著、歌词等。输出为json形式，内容为text，出处为author"
                                }
                            ]
                        })
                    });
                    
                    const data = await response.json();
                    
                    // 解析返回内容
                    let content = data.choices[0].message.content;
                    
                    // 检查是否包含json格式，如果是，提取json部分
                    let jsonMatch = content.match(/```json\s*([\s\S]*?)\s*```/) || content.match(/{[\s\S]*?}/);
                    let quoteData;
                    
                    if (jsonMatch) {
                        try {
                            quoteData = JSON.parse(jsonMatch[1] || jsonMatch[0]);
                        } catch (e) {
                            console.error("解析JSON失败:", e);
                            throw new Error("解析结果失败");
                        }
                    } else {
                        throw new Error("未找到有效的JSON数据");
                    }
                    
                    // 填充表单
                    contentInput.value = quoteData.text || "";
                    sourceInput.value = quoteData.author || "";
                    
                } catch (error) {
                    console.error("获取随机名言失败:", error);
                    alert("获取随机名言失败，请重试");
                } finally {
                    // 恢复按钮状态
                    randomBtn.textContent = '随机';
                    randomBtn.disabled = false;
                }
            });
        });
    </script>
</body>
</html> 
