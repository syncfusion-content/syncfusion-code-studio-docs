---
title: Documentation and Guides | BoldCreate
description: Learn how BoldCreate turns ideas into working software with AI assistance, team collaboration, enterprise governance, and cost management, all in one place.
platform: syncfusion-code-studio

---

# Welcome to BoldCreate Documentation

<style>
.section {
    background: #fff;
    margin: 0 0 24px;
    padding: 24px 44px 38px;
    border: 1px solid #e5e7eb;
    border-radius: 10px;
    scroll-margin-top: 88px;
}

.section-header {
    margin-bottom: 24px;
}

.section-header h2 {
    color: #302b30;
    font-size: 27px;
    line-height: 1.3;
    font-weight: 650;
    margin-top: 0 !important;
    margin-bottom: 9px;
}

.section-header p {
    color: #24466b;
    font-size: 15px;
    line-height: 1.7;
}

.card-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
}

.card {
    display: flex;
    flex-direction: column;
    min-height: 205px;
    background: #fff;
    border: 1px solid #e1e5e9;
    border-radius: 8px;
    color: inherit;
    text-decoration: none;
    overflow: hidden;
    transition: .2s ease;
}

.card:hover {
    border-color: #c8d1da;
    box-shadow: 0 5px 16px rgba(0,0,0,.06);
    transform: translateY(-1px);
}

.card,
.card:hover,
.card *,
.card:hover * {
    text-decoration: none !important;
}

.card-header {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 18px 20px;
    background: #fafcff;
    border-bottom: 1px solid #edf0f3;
}

.card-icon {
    width: 40px;
    height: 40px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    color: #0078d4;
    font-size: 26px;
    flex-shrink: 0;
}

.card-header h3 {
    flex: 1;
    color: #333;
    font-size: 16px;
    font-weight: 600;
}

.card-description {
    flex: 1;
    padding: 18px 20px 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.card-description p {
    color: #555;
    font-size: 14px;
    line-height: 1.65;
}

.card-link-text {
    margin-top: 15px;
    color: #0078d4;
    font-size: 13px;
    font-weight: 600;
}

.card-link-text::after {
    content: " →";
    transition: transform .2s ease;
}

.card:hover .card-link-text::after {
    display: inline-block;
    transform: translateX(3px);
}

@media (max-width: 760px) {
    .section { padding: 28px 22px; }
    .card-grid { grid-template-columns: 1fr; }
}
</style>

<p>BoldCreate is an AI-powered integrated development environment that combines intelligent code generation, smart workflow management, and enterprise-scale governance. BoldCreate helps teams build better software faster while maintaining control and quality.</p>

<p>Use this documentation to install BoldCreate, explore core features, configure your environment, manage teams and budgets, and integrate AI-assisted development into your applications.</p>

<section id="setup-section" class="section">
  <div class="section-header">
    <h2>Setup BoldCreate</h2>
    <p>Install BoldCreate, set up your team, and configure Enterprise Server for collaborative development.</p>
  </div>
  <div class="card-grid">

    <a href="/code/getting-started/install-and-configuration" class="card">
      <div class="card-header">
        <div class="card-icon">⚙️</div>
        <h3>Install and Configure IDE</h3>
      </div>
      <div class="card-description">
        <p>Download and install BoldCreate on your machine, sign in with your account, and activate your subscription.</p>
        <span class="card-link-text">Download</span>
      </div>
    </a>

    <a href="/code/teams-and-enterprise/userandteams" class="card">
      <div class="card-header">
        <div class="card-icon">👥</div>
        <h3>Set Up Teams and Users</h3>
      </div>
      <div class="card-description">
        <p>Invite team members, assign roles, and organize users into teams for seamless collaboration and governance.</p>
        <span class="card-link-text">Invite</span>
      </div>
    </a>

  </div>
</section>

<section id="ide-section" class="section">
  <div class="section-header">
    <h2>Build and Develop Smarter with AI</h2>
    <p>Develop intelligently with AI-powered coding assistance, structured workflows, and full customization capabilities.</p>
  </div>
  <div class="card-grid">

    <a href="/code/getting-started/quick-start" class="card">
      <div class="card-header">
        <div class="card-icon">🚀</div>
        <h3>Get Started Quickly</h3>
      </div>
      <div class="card-description">
        <p>Open your project, explore core AI features like Autocomplete, Ask, Edit, Agent, and Plan modes to accelerate your coding workflow.</p>
        <span class="card-link-text">Start</span>
      </div>
    </a>

    <a href="/code/agentic-toolbox/agent-guides/generate-your-first-code-using-agent" class="card">
      <div class="card-header">
        <div class="card-icon">💻</div>
        <h3>Generate Your First Code Change</h3>
      </div>
      <div class="card-description">
        <p>Enable Agent mode, describe your task, review AI-generated changes side-by-side, and use checkpoints to safely manage your code.</p>
        <span class="card-link-text">Generate</span>
      </div>
    </a>

    <a href="/code/agentic-toolbox/core-capabilities/project-manager" class="card">
      <div class="card-header">
        <div class="card-icon">📋</div>
        <h3>Structured Task Management</h3>
      </div>
      <div class="card-description">
        <p>Use Project Manager to break down complex objectives into clear stages: Define, Plan, Build, Verify, Review, and Ship your code.</p>
        <span class="card-link-text">Explore</span>
      </div>
    </a>

    <a href="/code/customize/custom-instructions" class="card">
      <div class="card-header">
        <div class="card-icon">⚙️</div>
        <h3>Customize Your IDE</h3>
      </div>
      <div class="card-description">
        <p>Define custom instructions, create project-level skills, configure custom agents, and tailor AI behavior to your team standards.</p>
        <span class="card-link-text">Customize</span>
      </div>
    </a>

  </div>
</section>

<section id="enterprise-section" class="section">
  <div class="section-header">
    <h2>Enterprise Governance and Analytics</h2>
    <p>Scale AI development across your organization with centralized administration, analytics, cost management, and compliance controls.</p>
  </div>
  <div class="card-grid">

    <a href="/code/monitoring-and-optimization/daily-cost-usage" class="card">
      <div class="card-header">
        <div class="card-icon">📊</div>
        <h3>Analytics and Monitoring</h3>
      </div>
      <div class="card-description">
        <p>Track daily AI usage, monitor token consumption, and analyze spending patterns across your organization in real-time.</p>
        <span class="card-link-text">Track</span>
      </div>
    </a>

    <a href="/code/teams-and-enterprise/createbudget" class="card">
      <div class="card-header">
        <div class="card-icon">💰</div>
        <h3>Budget and Cost Control</h3>
      </div>
      <div class="card-description">
        <p>Allocate budgets by team, set spending limits, and configure alerts to maintain control over AI costs.</p>
        <span class="card-link-text">Manage</span>
      </div>
    </a>

    <a href="/code/teams-and-enterprise/providersandmodels" class="card">
      <div class="card-header">
        <div class="card-icon">🤖</div>
        <h3>LLM Configuration</h3>
      </div>
      <div class="card-description">
        <p>Configure AI providers and models, manage default settings, and optimize your AI infrastructure for your organization.</p>
        <span class="card-link-text">Configure</span>
      </div>
    </a>

    <a href="/code/monitoring-and-optimization/buy-more-credits" class="card">
      <div class="card-header">
        <div class="card-icon">🛒</div>
        <h3>Buy More Credits</h3>
      </div>
      <div class="card-description">
        <p>Instantly add AI credits and keep your team development flowing without interruptions.</p>
        <span class="card-link-text">Purchase</span>
      </div>
    </a>

  </div>
</section>

<section id="resources-section" class="section">
  <div class="section-header">
    <h2>Learning Resources and Updates</h2>
    <p>Explore additional resources and stay updated with the latest BoldCreate features and best practices.</p>
  </div>
  <div class="card-grid">

    <a href="https://www.syncfusion.com/code-studio/handbooks" class="card">
      <div class="card-header">
        <div class="card-icon">📚</div>
        <h3>Handbooks</h3>
      </div>
      <div class="card-description">
        <p>Access comprehensive guides and best practices for getting the most out of BoldCreate.</p>
        <span class="card-link-text">Read</span>
      </div>
    </a>

    <a href="https://www.syncfusion.com/blogs/category/code-studio" class="card">
      <div class="card-header">
        <div class="card-icon">📰</div>
        <h3>Blog</h3>
      </div>
      <div class="card-description">
        <p>Read insights, tips, and best practices from our team and community members.</p>
        <span class="card-link-text">Explore</span>
      </div>
    </a>

    <a href="https://www.syncfusion.com/code-studio/whatsnew/" class="card">
      <div class="card-header">
        <div class="card-icon">✨</div>
        <h3>What New</h3>
      </div>
      <div class="card-description">
        <p>Explore the latest features and product updates in every BoldCreate release.</p>
        <span class="card-link-text">Discover</span>
      </div>
    </a>

    <a href="https://www.syncfusion.com/code-studio/self-service-demo/" class="card">
      <div class="card-header">
        <div class="card-icon">📹</div>
        <h3>Videos</h3>
      </div>
      <div class="card-description">
        <p>View interactive demos and self-paced video tutorials to learn BoldCreate and workflows.</p>
        <span class="card-link-text">Watch</span>
      </div>
    </a>

  </div>
</section>
