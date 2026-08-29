<style>
  .ai-agents-table-container {
    width: 100%;
    overflow-x: auto;
    margin: 1.5rem 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  }
  .ai-agents-table {
    width: 100%;
    border-collapse: collapse;
    text-align: left;
    font-size: 14px;
    line-height: 1.5;
    background-color: #16171a;
    color: #e2e8f0;
    border-radius: 12px;
  }
  .ai-agents-table th, 
  .ai-agents-table td {
    padding: 14px 18px;
    border-bottom: 1px solid #262930;
    vertical-align: middle;
  }
  .ai-agents-table thead th {
    background-color: #1f2228;
    color: #f8fafc;
    font-weight: 600;
    letter-spacing: 0.02em;
    white-space: nowrap;
  }
  .ai-agents-table tbody tr:hover {
    background-color: #1c1e24;
  }
  .ai-agents-table tbody tr:last-child td {
    border-bottom: none;
  }

  /* Dropdown Wrapper */
  .dropdown-wrapper {
    position: relative;
    display: inline-block;
  }

  /* Agent Trigger Button */
  .agent-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: linear-gradient(180deg, #2a2e37 0%, #20232a 100%);
    color: #f1f5f9;
    border: 1px solid #3b4252;
    padding: 7px 14px;
    font-size: 13px;
    font-weight: 500;
    border-radius: 8px;
    cursor: pointer;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.08);
    transition: all 0.2s ease;
    white-space: nowrap;
  }
  .agent-btn:hover {
    background: linear-gradient(180deg, #323742 0%, #262a33 100%);
    border-color: #60a5fa;
    color: #93c5fd;
    box-shadow: 0 0 0 3px rgba(96, 165, 250, 0.15);
  }
  .agent-btn svg.chevron {
    width: 10px;
    height: 10px;
    fill: none;
    stroke: currentColor;
    stroke-width: 2;
    stroke-linecap: round;
    transition: transform 0.25s ease;
  }
  .dropdown-wrapper:hover .agent-btn svg.chevron {
    transform: rotate(180deg);
  }

  /* Dropdown Menu with Hover Delay Mechanism */
  .dropdown-menu {
    position: absolute;
    top: 100%;
    left: 0;
    z-index: 60;
    min-width: 175px;
    padding: 6px;
    margin-top: 6px;
    background-color: #1e2128;
    border: 1px solid #333842;
    border-radius: 10px;
    box-shadow: 0 12px 30px -4px rgba(0, 0, 0, 0.65), 0 4px 10px rgba(0, 0, 0, 0.4);
    
    /* Disappear transition (1s delay when unhovered) */
    opacity: 0;
    visibility: hidden;
    transform: translateY(6px);
    transition: opacity 0.25s ease 1s, transform 0.25s ease 1s, visibility 0s 1.25s;
    pointer-events: none;
  }

  /* Seamless invisible bridge to prevent dropdown closing when moving mouse across margin */
  .dropdown-menu::before {
    content: '';
    position: absolute;
    top: -8px;
    left: 0;
    right: 0;
    height: 8px;
  }

  /* Appear transition (0.5s delay when hovered) */
  .dropdown-wrapper:hover .dropdown-menu {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
    pointer-events: auto;
    transition: opacity 0.25s ease 0.5s, transform 0.25s ease 0.5s, visibility 0s 0.5s;
  }

  /* Dropdown Items */
  .dropdown-item {
    display: flex;
    align-items: center;
    gap: 9px;
    padding: 8px 12px;
    color: #cbd5e1;
    text-decoration: none;
    font-size: 12.5px;
    font-weight: 500;
    border-radius: 6px;
    transition: all 0.15s ease;
  }
  .dropdown-item svg {
    width: 14px;
    height: 14px;
    fill: currentColor;
    flex-shrink: 0;
    color: #94a3b8;
    transition: color 0.15s ease;
  }
  .dropdown-item:hover {
    background-color: #2b303a;
    color: #60a5fa;
  }
  .dropdown-item:hover svg {
    color: #60a5fa;
  }
</style>

<div class="ai-agents-table-container">
  <table class="ai-agents-table">
    <thead>
      <tr>
        <th scope="col">AI Agent Platform</th>
        <th scope="col">Agent Type</th>
        <th scope="col">Key Capabilities</th>
        <th scope="col">Ideal Use Scenario</th>
        <th scope="col">Designed For</th>
      </tr>
    </thead>
    <tbody>
      <!-- Kimi AI Agent -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              Kimi AI Agent
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://www.kimi.ai/agent" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/MoonshotAI" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Autonomous AI agent[cite: 1]</td>
        <td>Deep research, code generation, data analysis, PPT/document creation, multi-source information processing, long-context reasoning[cite: 1]</td>
        <td>All-purpose AI tasks[cite: 1]</td>
        <td>Professionals, students, researchers, developers[cite: 1]</td>
      </tr>

      <!-- Hermes -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              Hermes
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://hermes-agent.nousresearch.com" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/nousresearch/hermes-agent" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Open-source agent framework[cite: 1]</td>
        <td>Custom workflows, external LLM connections, agent behavior control[cite: 1]</td>
        <td>Custom AI agent building[cite: 1]</td>
        <td>Developers, AI builders, automation projects[cite: 1]</td>
      </tr>

      <!-- OpenClaw -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              OpenClaw
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://openclaw.ai" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/openclaw/openclaw" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Open agent framework[cite: 1]</td>
        <td>Custom deployment, service integration, infrastructure control[cite: 1]</td>
        <td>Self-hosted agent workflows[cite: 1]</td>
        <td>Technical teams, researchers, experimenters[cite: 1]</td>
      </tr>

      <!-- AutoGPT -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              AutoGPT
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://agpt.co" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/Significant-Gravitas/AutoGPT" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Goal-driven AI agent[cite: 1]</td>
        <td>Task decomposition, autonomous planning, multi-step execution[cite: 1]</td>
        <td>Autonomous task execution[cite: 1]</td>
        <td>Automation, productivity workflows, AI experiments[cite: 1]</td>
      </tr>

      <!-- AutoGen -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              AutoGen
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://microsoft.github.io/autogen" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/microsoft/autogen" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Multi-agent system[cite: 1]</td>
        <td>Agent communication, role delegation, collaborative problem solving[cite: 1]</td>
        <td>Multi-agent collaboration[cite: 1]</td>
        <td>Enterprise AI, research, complex workflows[cite: 1]</td>
      </tr>

      <!-- CrewAI -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              CrewAI
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://www.crewai.com" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/crewAIInc/crewAI" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Multi-agent orchestration[cite: 1]</td>
        <td>Agent roles, task delegation, workflow coordination[cite: 1]</td>
        <td>Role-based agent teams[cite: 1]</td>
        <td>Business workflows, content teams, operations[cite: 1]</td>
      </tr>

      <!-- LangGraph -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              LangGraph
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://www.langchain.com/langgraph" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/langchain-ai/langgraph" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Stateful agent framework[cite: 1]</td>
        <td>Graph workflows, memory, conditional execution, and agent control[cite: 1]</td>
        <td>Building advanced AI agents[cite: 1]</td>
        <td>Developers, AI applications, complex systems[cite: 1]</td>
      </tr>

      <!-- n8n -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              n8n
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://n8n.io" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/n8n-io/n8n" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Automation + AI workflow platform[cite: 1]</td>
        <td>Visual workflows, API integrations, business process automation[cite: 1]</td>
        <td>Workflow automation[cite: 1]</td>
        <td>Businesses, marketing, internal tools[cite: 1]</td>
      </tr>

      <!-- LlamaIndex -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              LlamaIndex
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://www.llamaindex.ai" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/run-llama/llama_index" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Data-connected AI framework[cite: 1]</td>
        <td>RAG, document retrieval, data indexing, knowledge assistants[cite: 1]</td>
        <td>Knowledge-based AI systems[cite: 1]</td>
        <td>Enterprise search, document AI, data projects[cite: 1]</td>
      </tr>

      <!-- Flowise -->
      <tr>
        <td>
          <div class="dropdown-wrapper">
            <button class="agent-btn" type="button">
              Flowise
              <svg class="chevron" viewBox="0 0 10 6"><path d="M1 1L5 5L9 1"/></svg>
            </button>
            <div class="dropdown-menu">
              <a href="https://flowiseai.com" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
                Official Website
              </a>
              <a href="https://github.com/FlowiseAI/Flowise" target="_blank" rel="noopener noreferrer" class="dropdown-item">
                <svg viewBox="0 0 24 24"><path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z"/></svg>
                GitHub Repository
              </a>
            </div>
          </div>
        </td>
        <td>Visual AI agent builder[cite: 1]</td>
        <td>Drag-and-drop agent workflows, tool connections, and rapid prototyping[cite: 1]</td>
        <td>No-code AI workflow creation[cite: 1]</td>
        <td>Beginners, educators, prototype builders[cite: 1]</td>
      </tr>
    </tbody>
  </table>
</div>
