# 致李建裕老师 
---

---

<style>
/* ===== 全局样式 ===== */
:root {
  --primary: #2c3e50;        
  --accent: #e74c3c;         
  --light: #ecf0f1;         
  --gold: #f1c40f;          
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Noto Serif SC', serif, 'Microsoft YaHei', sans-serif;
  background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
  color: #34495e;
  line-height: 1.8;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  animation: gradientShift 20 ease infinite;
}

/* ===== 信纸容器 ===== */
.letter-container {
  max-width: 800px;
  background: rgba(255, 255, 255, 0.92);
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  position: relative;
  padding: 3rem;
  transform: translateY(20px);
  opacity: 0;
  animation: letterAppear 1.2 cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
  border-top: 4px solid var(--accent);
}

/* 信纸装饰元素 */
.letter-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 8px;
  background: linear-gradient(90deg, var(--accent), var(--gold), var(--accent));
}

/* ===== 动画效果 ===== */
@keyframes letterAppear {
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes gradientShift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

/* ===== 标题样式 ===== */
.letter-header {
  text-align: center;
  margin-bottom: 2.5rem;
  position: relative;
  padding-bottom: 1.5rem;
}

.letter-header h1 {
  font-size: 2.8rem;
  color: var(--primary);
  letter-spacing: 2px;
  margin-bottom: 0.5rem;
  font-weight: 700;
}

.letter-header h1::after {
  content: "";
  display: block;
  width: 80px;
  height: 4px;
  background: var(--gold);
  margin: 1rem auto;
  border-radius: 2px;
}

.letter-subtitle {
  font-size: 1.2rem;
  color: #7f8c8d;
  font-style: italic;
}

/* ===== 正文样式 ===== */
.letter-content {
  font-size: 1.1rem;
  position: relative;
  z-index: 2;
}

.letter-content p {
  margin-bottom: 1.5rem;
  text-align: justify;
  position: relative;
  padding-left: 2rem;
}

.letter-content p::before {
  content: "❝";
  position: absolute;
  left: 0;
  top: -0.8rem;
  color: rgba(231, 76, 60, 0.2);
  font-size: 3rem;
  font-family: serif;
}

/* 重点强调文本 */
.highlight {
  background: linear-gradient(transparent 60%, rgba(241, 196, 15, 0.3) 40%);
  font-weight: 600;
  padding: 0 4px;
}

/* ===== 落款样式 ===== */
.letter-signature {
  text-align: right;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px dashed #bdc3c7;
  animation: float 4 ease-in-out infinite;
}

.signature-name {
  font-size: 1.8rem;
  font-family: 'Dancing Script', cursive;
  color: var(--primary);
  margin-bottom: 0.5rem;
}

.signature-date {
  color: #7f8c8d;
  font-size: 1.1rem;
}

/* ===== 装饰元素 ===== */
.decorative-corner {
  position: absolute;
  width: 80px;
  height: 80px;
  opacity: 0.08;
}

.corner-tl { top: 20px; left: 20px; border-top: 2px solid var(--accent); border-left: 2px solid var(--accent); }
.corner-tr { top: 20px; right: 20px; border-top: 2px solid var(--accent); border-right: 2px solid var(--accent); }
.corner-bl { bottom: 20px; left: 20px; border-bottom: 2px solid var(--accent); border-left: 2px solid var(--accent); }
.corner-br { bottom: 20px; right: 20px; border-bottom: 2px solid var(--accent); border-right: 2px solid var(--accent); }

/* ===== 响应式设计 ===== */
@media (max-width: 768px) {
  body { padding: 1rem; }
  .letter-container { padding: 1.5rem; }
  .letter-header h1 { font-size: 2.2rem; }
  .letter-content { font-size: 1rem; }
}
</style>

<!-- 引入Google字体 -->
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;700&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">

<div class="letter-container">
  <!-- 装饰角 -->
  <div class="decorative-corner corner-tl"></div>
  <div class="decorative-corner corner-tr"></div>
  <div class="decorative-corner corner-bl"></div>
  <div class="decorative-corner corner-br"></div>
  
  <!-- 信头 -->
  <div class="letter-header">
    <h1>敬爱的李建裕老师</h1>
    <div class="letter-subtitle">计算机网络技术22113班学生留</div>
  </div>
  
  <!-- 信件内容 -->
  <div class="letter-content">
    <p>测试<span class="highlight"></span>。</p>

  </div>
  
  <!-- 落款 -->
  <div class="letter-signature">
    <div class="signature-name">22113</div>
    <div class="signature-date">2025年6月25日</div>
  </div>
</div>
