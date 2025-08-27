[![ReadMe](https://img.shields.io/badge/ReadMe-018EF5?logo=readme&logoColor=fff)](#)

# AI-Powered-Student-Mental-Health-Prediction-Support-System
A full-stack web application that leverages machine learning to proactively identify students at risk of mental health challenges and connect them with tailored support resources. The system analyzes academic, behavioral, and optional self-reported data to provide early interventions.

<img  alt="Tech Stack Badge" src="https://img.shields.io/badge/Stack-React%2520%252B%2520Spring%2520Boot%2520%252B%2520Python-blue?style=for-the-badge" />
<img  alt="Machine Learning Badge" src="https://img.shields.io/badge/ML-Transformer_XGBoost-Orange?style=for-the-badge&logo=python&logoColor=white&color=orange" />
<img  alt="Project Status Badge" src="https://img.shields.io/badge/Status-Proof%2520of%2520Concept-success?style=for-the-badge" />

## 🧠 Table of Contents
### Overview

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README List Solutions</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        header {
            background: #24292e;
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        header h1 {
            margin-bottom: 10px;
            font-size: 2.5rem;
        }
        
        header p {
            color: #c9d1d9;
            font-size: 1.1rem;
        }
        
        .github-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }
        
        .content {
            padding: 30px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        @media (max-width: 768px) {
            .content {
                grid-template-columns: 1fr;
            }
        }
        
        .card {
            background: #f6f8fa;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            border: 1px solid #e1e4e8;
        }
        
        .card h2 {
            color: #0366d6;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #0366d6;
        }
        
        .problem, .solution {
            margin-bottom: 20px;
        }
        
        .code-block {
            background: #1e1e1e;
            color: #d4d4d4;
            padding: 15px;
            border-radius: 5px;
            font-family: 'Consolas', monospace;
            overflow-x: auto;
            margin: 15px 0;
        }
        
        .code-block code {
            display: block;
            white-space: pre-wrap;
        }
        
        .tag {
            color: #569cd6;
        }
        
        .attribute {
            color: #9cdcfe;
        }
        
        .value {
            color: #ce9178;
        }
        
        .comment {
            color: #6a9955;
        }
        
        .result {
            background: white;
            padding: 15px;
            border-radius: 5px;
            border-left: 4px solid #28a745;
            margin: 15px 0;
        }
        
        .result ul, .result ol {
            margin: 10px 0 10px 20px;
        }
        
        .result li {
            margin-bottom: 5px;
        }
        
        .note {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        
        .tip {
            background: #d1ecf1;
            border-left: 4px solid #0dcaf0;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background: #24292e;
            color: white;
        }
        
        .try-button {
            display: inline-block;
            background: #0366d6;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 10px;
            transition: background 0.3s;
        }
        
        .try-button:hover {
            background: #0356b6;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="github-icon">🐙</div>
            <h1>HTML Lists in GitHub README</h1>
            <p>Solving the issue with &lt;ul&gt; and &lt;ol&gt; tags not rendering properly</p>
        </header>
        
        <div class="content">
            <div class="card">
                <h2>The Problem</h2>
                <div class="problem">
                    <p>When you use HTML list tags in your README.md file:</p>
                    <div class="code-block">
                        <code><span class="tag">&lt;ul&gt;</span>
    <span class="tag">&lt;li&gt;</span>First item<span class="tag">&lt;/li&gt;</span>
    <span class="tag">&lt;li&gt;</span>Second item<span class="tag">&lt;/li&gt;</span>
    <span class="tag">&lt;li&gt;</span>Third item<span class="tag">&lt;/li&gt;</span>
<span class="tag">&lt;/ul&gt;</span></code>
                    </div>
                    <p>GitHub might not render them correctly because:</p>
                    <ul>
                        <li>GitHub Flavored Markdown has limitations on HTML support</li>
                        <li>Some HTML tags are sanitized for security reasons</li>
                        <li>Improperly formatted HTML might not be rendered</li>
                    </ul>
                </div>
                
                <div class="note">
                    <strong>Note:</strong> GitHub does support some HTML tags in Markdown, but it's inconsistent. For reliability, use Markdown syntax instead.
                </div>
            </div>
            
            <div class="card">
                <h2>The Solution</h2>
                <div class="solution">
                    <p>Use Markdown syntax for lists instead of HTML:</p>
                    <div class="code-block">
                        <code><span class="comment"># For unordered lists</span>
- Item one
- Item two
- Item three

<span class="comment"># For ordered lists</span>
1. First item
2. Second item
3. Third item</code>
                    </div>
                    
                    <p>This will render as:</p>
                    <div class="result">
                        <p><strong>Unordered list:</strong></p>
                        <ul>
                            <li>Item one</li>
                            <li>Item two</li>
                            <li>Item three</li>
                        </ul>
                        
                        <p><strong>Ordered list:</strong></p>
                        <ol>
                            <li>First item</li>
                            <li>Second item</li>
                            <li>Third item</li>
                        </ol>
                    </div>
                </div>
                
                <div class="tip">
                    <strong>Pro Tip:</strong> You can create nested lists by indenting items with 2 or 4 spaces.
                </div>
            </div>
            
            <div class="card">
                <h2>Nested Lists Example</h2>
                <div class="code-block">
                    <code><span class="comment"># Nested list example</span>
- Main item 1
  - Subitem 1.1
  - Subitem 1.2
- Main item 2
  - Subitem 2.1
  - Subitem 2.2</code>
                </div>
                
                <p>This will render as:</p>
                <div class="result">
                    <ul>
                        <li>Main item 1
                            <ul>
                                <li>Subitem 1.1</li>
                                <li>Subitem 1.2</li>
                            </ul>
                        </li>
                        <li>Main item 2
                            <ul>
                                <li>Subitem 2.1</li>
                                <li>Subitem 2.2</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="card">
                <h2>Task Lists Example</h2>
                <p>GitHub also supports special task lists:</p>
                <div class="code-block">
                    <code><span class="comment"># Task list example</span>
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task</code>
                </div>
                
                <p>This will render as:</p>
                <div class="result">
                    <ul>
                        <li><input type="checkbox" checked disabled> Completed task</li>
                        <li><input type="checkbox" disabled> Incomplete task</li>
                        <li><input type="checkbox" disabled> Another task</li>
                    </ul>
                </div>
                
                <div class="tip">
                    <strong>Pro Tip:</strong> Task lists are great for tracking project progress directly in your README.
                </div>
            </div>
        </div>
        
        <div class="note" style="margin: 30px;">
            <h3>When you must use HTML in Markdown</h3>
            <p>If you absolutely need to use HTML lists in your README (for specific styling or attributes), ensure they are properly formatted and closed. Some HTML tags work in GitHub Markdown, but always test to make sure they render correctly.</p>
            <a href="https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax" class="try-button" target="_blank">GitHub Formatting Guide</a>
        </div>
        
        <footer>
            <p>Solved HTML list rendering issues in GitHub README.md files | Format using Markdown instead of HTML</p>
        </footer>
    </div>
</body>
</html>
