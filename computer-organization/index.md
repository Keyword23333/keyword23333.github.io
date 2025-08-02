---
layout: default
title: "计算机组成原理"
---

<div class="course-homepage">
  <header>
    <h1>{{ page.title }}</h1>
    <p >{{ site.data.chapters.course_info.subtitle }}</p>
    <p >{{ site.data.chapters.course_info.description }}</p>
  </header>

  <div class="course-overview">
    <div class="course-stats">
      <div class="stat-item">
        <span class="stat-number">{{ site.data.chapters.course_info.total_chapters }}</span>
        <span class="stat-label">章节</span>
      </div>
      <div class="stat-item">
        <span class="stat-number">7</span>
        <span class="stat-label">主题</span>
      </div>
      <div class="stat-item">
        <span class="stat-number">完整</span>
        <span class="stat-label">课程</span>
      </div>
    </div>

    <div class="course-chapters">
      <h2>课程章节</h2>
      <div class="chapter-grid">
        {% for chapter in site.data.chapters.chapters %}
          <div class="chapter-card">
            <div class="chapter-number">{{ forloop.index }}</div>
            <div class="chapter-content">
              <h3>{{ chapter.title }}</h3>
              <p>{{ chapter.description }}</p>
              <a href="{{ chapter.url }}" class="chapter-btn">开始学习</a>
            </div>
          </div>
        {% endfor %}
      </div>
    </div>

    <div class="course-features">
      <h2>课程特色</h2>
      <div class="features-grid">
        <div class="feature-item">
          <div class="feature-icon">📚</div>
          <h3>系统性强</h3>
          <p>从基础概念到高级应用，循序渐进地学习计算机组成原理</p>
        </div>
        <div class="feature-item">
          <div class="feature-icon">💻</div>
          <h3>实践导向</h3>
          <p>结合实例和代码，深入理解计算机硬件工作原理</p>
        </div>
        <div class="feature-item">
          <div class="feature-icon">🎯</div>
          <h3>重点突出</h3>
          <p>突出核心概念和关键知识点，帮助快速掌握要点</p>
        </div>
        <div class="feature-item">
          <div class="feature-icon">📈</div>
          <h3>进度跟踪</h3>
          <p>实时显示学习进度，激励持续学习</p>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
.course-homepage {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
}

.course-header {
  text-align: center;
  margin-bottom: 60px;
}

.course-header h1 {
  font-size: 3em;
  margin: 0 0 10px 0;
  color: var(--headings);
}

.course-subtitle {
  font-size: 1.5em;
  color: var(--text-secondary);
  margin: 0 0 20px 0;
}

.course-description {
  font-size: 1.2em;
  color: var(--text);
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.course-stats {
  display: flex;
  justify-content: center;
  gap: 40px;
  margin-bottom: 60px;
}

.stat-item {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2.5em;
  font-weight: bold;
  color: var(--links);
}

.stat-label {
  color: var(--text-secondary);
  font-size: 1.1em;
}

.course-chapters {
  margin-bottom: 60px;
}

.course-chapters h2 {
  text-align: center;
  margin-bottom: 40px;
  color: var(--headings);
  font-size: 2em;
}

.chapter-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.chapter-card {
  background: var(--bg-secondary);
  border-radius: 12px;
  padding: 25px;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.chapter-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

.chapter-number {
  position: absolute;
  top: 15px;
  right: 15px;
  width: 40px;
  height: 40px;
  background: var(--links);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2em;
}

.chapter-content h3 {
  margin: 0 0 15px 0;
  color: var(--headings);
  font-size: 1.3em;
}

.chapter-content p {
  margin: 0 0 20px 0;
  color: var(--text);
  line-height: 1.6;
}

.chapter-btn {
  display: inline-block;
  padding: 10px 20px;
  background: var(--links);
  color: white;
  text-decoration: none;
  border-radius: 6px;
  transition: all 0.2s ease;
  font-weight: 500;
}

.chapter-btn:hover {
  background: var(--headings);
  transform: translateY(-2px);
}

.course-features {
  margin-top: 80px;
}

.course-features h2 {
  text-align: center;
  margin-bottom: 40px;
  color: var(--headings);
  font-size: 2em;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
}

.feature-item {
  text-align: center;
  padding: 30px 20px;
  background: var(--bg-secondary);
  border-radius: 12px;
  transition: all 0.3s ease;
}

.feature-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
}

.feature-icon {
  font-size: 3em;
  margin-bottom: 20px;
}

.feature-item h3 {
  margin: 0 0 15px 0;
  color: var(--headings);
  font-size: 1.3em;
}

.feature-item p {
  margin: 0;
  color: var(--text);
  line-height: 1.6;
}

@media (max-width: 768px) {
  .course-header h1 {
    font-size: 2.5em;
  }
  
  .course-stats {
    flex-direction: column;
    gap: 20px;
  }
  
  .chapter-grid {
    grid-template-columns: 1fr;
  }
  
  .features-grid {
    grid-template-columns: 1fr;
  }
}
</style> 