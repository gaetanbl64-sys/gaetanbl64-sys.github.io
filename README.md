<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaëtan Baylou-Lanot | Portfolio</title>
    <style>
        :root {
            --bg-main: #0f172a;
            --bg-sidebar: #1e293b;
            --bg-card: #1e293b;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --accent: #38bdf8;
            --accent-hover: #7dd3fc;
            --border: #334155;
            --code-bg: #0f172a;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            color: var(--text-main);
            background-color: var(--bg-main);
            margin: 0;
            padding: 0;
            display: flex;
            line-height: 1.7;
        }

        /* Sidebar Navigation */
        .sidebar {
            width: 320px;
            background-color: var(--bg-sidebar);
            border-right: 1px solid var(--border);
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            padding: 3rem 1.5rem;
            box-sizing: border-box;
            overflow-y: auto;
        }

        .profile {
            text-align: center;
            margin-bottom: 2.5rem;
            border-bottom: 1px solid var(--border);
            padding-bottom: 2rem;
        }

        .profile-pic {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #38bdf8, #6366f1);
            border-radius: 50%;
            margin: 0 auto 1.2rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            box-shadow: 0 4px 12px rgba(56, 189, 248, 0.2);
        }

        .profile h1 {
            font-size: 1.25rem;
            margin: 0;
            font-weight: 700;
            letter-spacing: -0.025em;
        }

        .profile p {
            font-size: 0.85rem;
            color: var(--text-muted);
            margin: 0.5rem 0 0 0;
        }

        .nav-links {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .nav-links li {
            margin-bottom: 0.4rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-muted);
            font-weight: 500;
            font-size: 0.9rem;
            display: block;
            padding: 0.6rem 0.8rem;
            border-radius: 8px;
            transition: evils 0.2s ease;
        }

        .nav-links a:hover {
            background-color: rgba(255, 255, 255, 0.05);
            color: var(--accent);
        }

        /* Main Content Area */
        .content {
            margin-left: 320px;
            padding: 4rem 5rem;
            max-width: 900px;
            width: 100%;
            box-sizing: border-box;
        }

        .header-section {
            margin-bottom: 3.5rem;
        }

        h1 {
            font-size: 2.5rem;
            font-weight: 800;
            letter-spacing: -0.04em;
            margin: 0 0 0.75rem 0;
            background: linear-gradient(to right, #fff, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .meta {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* Project Cards */
        .project-card {
            background-color: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 2rem;
            margin-bottom: 2.5rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .project-card h2 {
            font-size: 1.4rem;
            color: var(--text-main);
            margin-top: 0;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        p {
            color: var(--text-muted);
            margin: 0 0 1.25rem 0;
            font-size: 0.95rem;
        }

        ul {
            padding-left: 1.25rem;
            margin: 0 0 1.5rem 0;
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        li {
            margin-bottom: 0.5rem;
        }

        /* Technology Badges */
        .tag-container {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.2rem;
        }

        .tag {
            background: rgba(56, 189, 248, 0.1);
            color: var(--accent);
            padding: 0.2rem 0.6rem;
            border-radius: 6px;
            font-size: 0.75rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .tag.personal {
            background: rgba(168, 85, 247, 0.1);
            color: #c084fc;
        }

        /* Code Block Styling */
        pre {
            background-color: var(--code-bg);
            padding: 1.2rem;
            border-radius: 8px;
            overflow-x: auto;
            border: 1px solid var(--border);
            margin: 1.5rem 0 0 0;
        }

        code {
            font-family: "SFMono-Regular", Consolas, monospace;
            font-size: 0.85rem;
            color: #f43f5e;
        }

        pre code {
            color: #e2e8f0;
        }

        blockquote {
            border-left: 4px solid var(--accent);
            margin: 1.5rem 0;
            padding: 0.5rem 1rem;
            background-color: rgba(56, 189, 248, 0.03);
            color: var(--text-muted);
            border-radius: 0 8px 8px 0;
        }

        /* Responsive Layout */
        @media (max-width: 992px) {
            body { flex-direction: column; }
            .sidebar { width: 100%; height: auto; position: relative; border-right: none; border-bottom: 1px solid var(--border); padding: 2rem 1.5rem; }
            .content { margin-left: 0; padding: 2rem 1.5rem; }
        }
    </style>
</head>
<body>

    <!-- SIDEBAR NAVIGATION -->
    <div class="sidebar">
        <div class="profile">
            <div class="profile-pic">🤖</div>
            <h1>Gaëtan Baylou-Lanot</h1>
            <p>Robotics & AI Engineer Portfolio</p>
        </div>
        <ul class="nav-links">
            <li><a href="#about">📌 About & Internships</a></li>
            <li><a href="#ros2-control">🔌 Robot Control (ROS2)</a></li>
            <li><a href="#ia-rl">🤖 Robot Guidance (RL)</a></li>
            <li><a href="#cpp-club">⚙️ Robotics Club (C++)</a></li>
            <li><a href="#ia-ml">🧠 Supervised Learning</a></li>
            <li><a href="#van-conversion">🚐 Van Conversion</a></li>
        </ul>
    </div>

    <!-- MAIN CONTENT -->
    <div class="content">
        
        <div class="header-section">
            <h1>Engineering Portfolio</h1>
            <div class="meta">Last updated: 2026 • By Gaëtan Baylou-Lanot</div>
            <blockquote>
                Welcome to my project showcase. This documentation technical page deeper dives into the architecture, codebase, and methodologies of my main engineering projects.
            </blockquote>
        </div>

        <!-- SECTION 1: ABOUT & INTERNSHIPS -->
        <section id="about" class="project-card">
            <h2>📌 My Study: 3 Internships</h2>
            <p>A quick chronological overview of my professional experiences in the industry, linking academic knowledge to concrete engineering solutions.</p>
            <ul>
                <li><strong>Internship 3 (Latest):</strong> [Company Name] — Working on [Main Topic/Technology]. Deep dive into production-ready software engineering.</li>
                <li><strong>Internship 2:</strong> [Company Name] — Focused on [Main Topic/Technology]. Developing core components and system integration.</li>
                <li><strong>Internship 1:</strong> [Company Name] — Initial industry experience dealing with [Main Topic/Technology].</li>
            </ul>
        </section>

        <!-- SECTION 2: ROS2 -->
        <section id="ros2-control" class="project-card">
            <h2>🔌 Code project n°2: robot control with ROS2</h2>
            <div class="tag-container">
                <span class="tag">ROS2</span>
                <span class="tag">C++ / Python</span>
                <span class="tag">Linux</span>
            </div>
            <p>Implementation of an advanced middleware control architecture using Robot Operating System 2 to drive autonomous mobile units.</p>
            <ul>
                <li>Designed custom ROS2 Nodes with optimized publisher/subscriber patterns.</li>
                <li>Handled real-time sensor fusion (LiDAR, Odometry, IMU) for navigation mapping.</li>
                <li>Managed lifecycle nodes and custom services for robust fail-safe states.</li>
            </ul>
        </section>

        <!-- SECTION 3: RL -->
        <section id="ia-rl" class="project-card">
            <h2>🤖 IA project n°2: simulation and guidance of robot by RL</h2>
            <div class="tag-container">
                <span class="tag">Reinforcement Learning</span>
                <span class="tag">Python</span>
                <span class="tag">Gym/Gazebo</span>
            </div>
            <p>Developing a deep reinforcement learning pipeline allowing a simulated agent to safely navigate complex environments.</p>
            <ul>
                <li>Created custom simulation environments using Gym wrappers and physics engines.</li>
                <li>Designed and fine-tuned reward functions to prevent collisions while maximizing velocity.</li>
                <li>Evaluated policy gradient methods (PPO, DDPG) regarding training convergence times.</li>
            </ul>
        </section>

        <!-- SECTION 4: C++ CLUB -->
        <section id="cpp-club" class="project-card">
            <h2>⚙️ Code projet n°1: robotics' club in C++</h2>
            <div class="tag-container">
                <span class="tag">C++17</span>
                <span class="tag">Embedded Systems</span>
                <span class="tag">Git</span>
            </div>
            <p>Core software development for the competitive team at the robotics club, building modular firmware from scratch.</p>
            <ul>
                <li>Wrote clean, object-oriented C++ code for low-level microcontrollers and motor drivers.</li>
                <li>Implemented precise interrupt-driven sensor polling routines.</li>
                <li>Maintained repository structure and continuous integration using Git workflows.</li>
            </ul>
        </section>

        <!-- SECTION 5: ML SUPERVISED -->
        <section id="ia-ml" class="project-card">
            <h2>🧠 IA project n°1: deployment of a supervised learning of food</h2>
            <div class="tag-container">
                <span class="tag">Computer Vision</span>
                <span class="tag">TensorFlow</span>
                <span class="tag">Deep Learning</span>
            </div>
            <p>End-to-end computer vision project focused on dataset processing, model training, and embedded deployment for real-time food classification.</p>
            <ul>
                <li>Curated, cleaned, and augmented an image dataset to resolve class imbalance.</li>
                <li>Trained a Convolutional Neural Network (CNN) achieving high accuracy metrics.</li>
            </ul>
<pre><code>import tensorflow as tf
from tensorflow.keras import layers, models

def build_vision_pipeline(input_shape, num_classes):
    """ Convolutional neural network structure for embedded classification """
    model = models.Sequential([
        layers.Conv2D(32, (3, 3), activation='relu', input_shape=input_shape),
        layers.MaxPooling2D((2, 2)),
        layers.Conv2D(64, (3, 3), activation='relu'),
        layers.Flatten(),
        layers.Dense(num_classes, activation='softmax')
    ])
    return model

print("Vision pipeline structure successfully compiled.")</code></pre>
        </section>

        <!-- SECTION 6: VAN CONVERSION -->
        <section id="van-conversion" class="project-card">
            <h2>🚐 Van conversion: bref summary of my personality</h2>
            <div class="tag-container">
                <span class="tag personal">Personal Project</span>
                <span class="tag personal">Project Management</span>
                <span class="tag personal">Engineering</span>
            </div>
            <p>Aside from pure software engineering, I spent months designing and building a completely autonomous off-grid campervan. This project highlights my practical problem-solving skills and hardware resourcefulness.</p>
            <ul>
                <li>Calculated and engineered a 12V solar electrical grid system with lithium battery storage.</li>
                <li>Created 3D CAD mockups for mechanical and spacing optimization.</li>
                <li>Demonstrated high resilience, adaptability, and budget management skills throughout the build.</li>
            </ul>
        </section>

    </div>

</body>
</html>
