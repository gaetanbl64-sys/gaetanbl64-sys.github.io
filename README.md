<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaëtan Baylou-Lanot - Project Portfolio</title>
    <style>
        /* ==========================================================================
           ARTISTIC DIRECTION: CHIRPY INSPIRED (MINIMALIST & LAB STYLE)
           ========================================================================== */
        :root {
            --bg-color: #ffffff;
            --text-color: #343a40;
            --heading-color: #1c1f23;
            --sidebar-bg: #f4f6f8;
            --sidebar-text: #495057;
            --accent-color: #007bff;
            --accent-bg-light: #e3f2fd;
            --code-bg: #1e1e1e;
            --code-text: #f8f8f2;
            --border-color: #dbdfe2;
            --tag-bg: #eff1f3;
            --tag-text: #6c757d;
        }

        body {
            font-family: "-apple-system", BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            color: var(--text-color);
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            -webkit-font-smoothing: antialiased;
        }

        /* LEFT SIDEBAR (COMPACT & CLEAN) */
        .sidebar {
            width: 240px;
            background-color: var(--sidebar-bg);
            border-right: 1px solid var(--border-color);
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 3rem 1.2rem 1.5rem 1.2rem;
            box-sizing: border-box;
            z-index: 100;
        }

        .sidebar-top {
            display: flex;
            flex-direction: column;
        }

        .profile {
            text-align: left;
            margin-bottom: 2.5rem;
            padding-left: 0.5rem;
        }

        .profile-pic {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, #e0e0e0, #f5f5f5);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-bottom: 1rem;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.05);
        }

        .profile h1 {
            font-size: 1.15rem;
            font-weight: 700;
            margin: 0;
            color: var(--heading-color);
            letter-spacing: -0.025em;
        }

        .profile p {
            font-size: 0.8rem;
            color: #868e96;
            margin: 0.3rem 0 0 0;
            font-weight: 400;
        }

        .nav-links {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .nav-links li {
            margin-bottom: 0.2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--sidebar-text);
            font-weight: 500;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 0.5rem 0.6rem;
            border-radius: 6px;
            transition: all 0.15s ease-in-out;
        }

        .nav-links a:hover {
            background-color: #e9ecef;
            color: var(--heading-color);
        }

        .sidebar-footer {
            display: flex;
            gap: 15px;
            padding-left: 0.6rem;
            font-size: 0.9rem;
            color: #adb5bd;
        }
        
        .sidebar-footer a {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.2s;
        }
        .sidebar-footer a:hover { color: var(--heading-color); }

        /* MAIN CONTENT AREA */
        .content {
            margin-left: 240px;
            padding: 3rem 2.5rem 3rem 1.5rem;
            max-width: 800px;
            box-sizing: border-box;
        }

        /* Chirpy Style Tags */
        .tag-container {
            margin-bottom: 0.75rem;
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }

        .tag {
            background: var(--tag-bg);
            color: var(--tag-text);
            padding: 0.15rem 0.55rem;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 500;
            transition: background 0.2s;
        }
        
        .tag:hover {
            background: #e2e6ea;
            color: var(--heading-color);
        }

        h1.main-title { 
            font-size: 2.2rem; 
            font-weight: 700;
            color: var(--heading-color);
            margin: 0 0 0.6rem 0;
            letter-spacing: -0.03em;
            line-height: 1.2;
        }

        .meta {
            font-size: 0.85rem;
            color: #868e96;
            margin-bottom: 2.5rem;
            padding-bottom: 1.2rem;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            gap: 15px;
        }

        h2 { 
            font-size: 1.45rem; 
            font-weight: 600;
            color: var(--heading-color);
            margin-top: 3.5rem; 
            margin-bottom: 1rem;
            letter-spacing: -0.02em;
        }

        p {
            margin: 1rem 0;
            color: var(--text-color);
            font-size: 1rem;
            line-height: 1.6;
        }

        ul {
            padding-left: 1.25rem;
            margin: 1rem 0;
        }

        li {
            margin-bottom: 0.6rem;
            color: var(--text-color);
            line-height: 1.5;
        }
        
        li strong {
            color: var(--heading-color);
        }

        /* PORTFOLIO IMAGES STYLE */
        .project-img {
            width: 100%;
            max-height: 350px;
            object-fit: cover;
            border-radius: 8px;
            margin: 1.2rem 0;
            box-shadow: 0 4px 10px rgba(0,0,0,0.06);
            border: 1px solid var(--border-color);
        }

        /* INFO ALERT BOX */
        blockquote.prompt-info {
            border-left: 4px solid var(--accent-color);
            margin: 2rem 0;
            padding: 1rem 1.25rem;
            background-color: var(--accent-bg-light);
            color: #1e4265;
            border-radius: 0 6px 6px 0;
            font-size: 0.95rem;
            display: flex;
            align-items: flex-start;
            gap: 10px;
        }
        
        blockquote.prompt-info::before {
            content: "ℹ️";
            font-size: 1.1rem;
            line-height: 1;
        }

        /* CODE BLOCKS */
        pre {
            background-color: var(--code-bg);
            padding: 1.25rem;
            border-radius: 8px;
            overflow-x: auto;
            margin: 1.75rem 0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }

        code {
            font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
            font-size: 0.85rem;
            background-color: #f1f3f5;
            color: #d63384;
            padding: 0.2rem 0.4rem;
            border-radius: 4px;
        }

        pre code {
            color: var(--code-text);
            background-color: transparent;
            padding: 0;
            border-radius: 0;
        }

        /* RESPONSIVE DESIGN */
        @media (max-width: 850px) {
            .sidebar { width: 100%; height: auto; position: relative; padding: 2rem 1.5rem; border-right: none; border-bottom: 1px solid var(--border-color); }
            .content { margin-left: 0; padding: 2.5rem 1.5rem; }
        }
    </style>
</head>
<body>

    <!-- LEFT SIDEBAR -->
    <div class="sidebar">
        <div class="sidebar-top">
            <div class="profile">
                <div class="profile-pic">🚀</div>
                <h1>Gaëtan Baylou-Lanot</h1>
                <p>Mechanical & Control Engineering Student</p>
            </div>
            <ul class="nav-links">
                <li><a href="#introduction">📌 Introduction</a></li>
                <li><a href="#van-conversion">🚐 Van Conversion</a></li>
                <li><a href="#my-internships">🎓 My Internships & Experience</a></li>
                <li><a href="#ins-aerien">✈️ Association INS'Aérien</a></li>
                <li><a href="#code-project-1">⚙️ Code Project n°1 (C++)</a></li>
                <li><a href="#code-project-2">🔌 Code Project n°2 (MATLAB)</a></li>
                <li><a href="#ia-project-1">🧠 AI Project n°1 (PPO & RL)</a></li>
                <li><a href="#volunteering">🤝 Leadership & Volunteering</a></li>
            </ul>
        </div>
        
        <div class="sidebar-footer">
            <a href="https://www.linkedin.com/in/gaetan-baylou-lanot-72931b177/" target="_blank" title="LinkedIn">🔗</a>
            <a href="mailto:Gaetan.baylou--lanot@insa-rennes.fr" title="Mail">✉️</a>
            <a href="https://canva.link/ky3nhbgvb7r8ahv" target="_blank" title="CV / Portfolio Link">📄</a>
        </div>
    </div>

    <!-- MAIN CONTENT AREA -->
    <div class="content">
        <div class="tag-container">
            <span class="tag">robotics</span>
            <span class="tag">reinforcement-learning</span>
            <span class="tag">control-engineering</span>
            <span class="tag">3d-printing</span>
            <span class="tag">embedded-systems</span>
        </div>
        
        <h1 class="main-title">Engineering Track & Technical Portfolio</h1>
        <div class="meta">
            <span>Current Year: 2026</span>
            <span>•</span>
            <span>Rennes, Bretagne, France</span>
        </div>

        <section id="introduction">
            <h2>📌 Introduction</h2>
            <p>I am a passionate, curious, and versatile engineering student specializing in <strong>Mechanical and Control Engineering (GMA)</strong> at <strong>INSA Rennes</strong>[cite: 1]. My core technical drivers lie at the intersection of outdoor sports, robotics, and complex automated control architectures[cite: 1]. I am currently actively seeking a challenging 4 to 5-month final-year internship in AI and robotics starting in March[cite: 1].</p>
            
            <blockquote class="prompt-info">
                <span>As documented in my official resume profile, I have a proven track record of managing technical timelines under high pressure, highlighted by competing in international robotics leagues[cite: 1].</span>
            </blockquote>
        </section>

        <!-- VAN CONVERSION SECTION -->
        <section id="van-conversion">
            <h2>🚐 Van conversion: A brief summary of my personality</h2>
            <p>Converting a van from scratch serves as a concrete manifestation of my engineering mindset outside the classroom. It outlines my resourcefulness, structural optimization skills, and capability to transition raw blueprints into robust physical installations.</p>
            
            <!-- Replace src with your local photo path (e.g., images/my_van.jpg) -->
            <img class="project-img" src="https://images.unsplash.com/photo-1527786356257-b271241f2f8a?auto=format&fit=crop&w=800&q=80" alt="Van Conversion Framework">

            <ul>
                <li><strong>Spatial Design:</strong> Drafted comprehensive 3D system assemblies to maximize volumetric efficiency within compact tolerances.</li>
                <li><strong>Embedded Infrastructure:</strong> Formulated off-grid electrical wire harnesses coupled with automated safety breakers and solar charger controls.</li>
                <li><strong>Material Science:</strong> Researched composite and layered insulation thermal profiles to handle unpredictable outdoor environments.</li>
            </ul>
        </section>

        <!-- MOVED & ENRICHED INTERNSHIPS SECTION -->
        <section id="my-internships">
            <h2>🎓 My Internships & Experience</h2>
            <p>Through my academic progression at INSA Rennes (2022 – 2027), I have consolidated theoretical system controls with structural, additive, and autonomous R&D placements across industrial domains[cite: 1]:</p>
            
            <ul>
                <li>
                    <strong>Scalian (June 2026 - Present) | AI Implementation Internship:</strong> 
                    Currently modelling and optimizing a ‘Duckiebot’ robot inside simulation environments to train, improve, and evaluate advanced reinforcement learning algorithms, specifically focusing on Proximal Policy Optimization (PPO)[cite: 1]. My responsibilities include granular adjustments of hyperparameter baselines and structural reward functions to safely transition training policies into physical robot guidance[cite: 1].
                </li>
                <li>
                    <strong>XSun (June 2025 - August 2025) | Structural Engineer Internship:</strong> 
                    Conducted conceptual studies regarding specialized lightweight structural materials, 3D parametric solid modelling, and complex technical drawings for the structural frame of a next-generation solar-powered VTOL drone model[cite: 1].
                </li>
                <li>
                    <strong>Decathlon France (July 2023 - August 2023) | 3D Technical Specialist:</strong> 
                    Operated within Decathlon's flagship ADDLAB laboratory facility[cite: 1]. Oversaw precision resin 3D printing workflows from software parameterization to physical finishing treatments, and executed core R&D testing pipelines to validate a new experimental compound for Selective Laser Sintering (SLS)[cite: 1]. Collaborated on frontier projects including prototype carbon-bicycle frames and bespoke component designs destined for the European Space Agency (ESA)[cite: 1].
                </li>
                <li>
                    <strong>Safran / Metallicadour (April 2019) | Robotic Arm R&D Placement:</strong> 
                    Embedded within the Metallicadour laboratory facility to shadow advanced research targeting automated aerospace workflows utilizing industrial KUKA robotic arms[cite: 1].
                </li>
                <li>
                    <strong>Private Academic Tutor (November 2024 - April 2025):</strong> 
                    Provided targeted, high-level Mathematics and Physics instruction to final-year high school students in Rennes, clarifying complex theoretical models[cite: 1].
                </li>
            </ul>
        </section>

        <!-- INS'AERIEN ASSOCIATION SECTION -->
        <section id="ins-aerien">
            <h2>✈️ President & Founder of the INS'Aérien Association</h2>
            <p>From September 2023 to December 2025, I spearheaded the creation and structural organization of INS'Aérien, a high-performance FPV drone club[cite: 1]. This initiative allowed me to combine complex hardware assemblies with creative video direction[cite: 1].</p>

            <img class="project-img" src="https://images.unsplash.com/photo-1508614589041-895b88991e3e?auto=format&fit=crop&w=800&q=80" alt="Custom Built FPV Drone">

            <ul>
                <li><strong>Hardware Engineering:</strong> Hand-built custom FPV drone configurations capable of extreme acceleration profiles, launching from 0 to 100 km/h in 2.2 seconds[cite: 1].</li>
                <li><strong>Operational Scale:</strong> Managed a dedicated crew of nine active members, successfully building three bespoke drone units from the ground up[cite: 1].</li>
                <li><strong>Production Delivery:</strong> Offered technical aerial cinematography services for commercial festivals and music videos, outputting more than 20 professional video clips using Adobe Premiere and Lightroom[cite: 1].</li>
                <li><strong>Executive Leadership:</strong> Gained extensive leadership insight regarding financial budgeting, administrative safety compliance, and inter-team communications[cite: 1].</li>
            </ul>
        </section>

        <!-- CODE PROJECT 1 -->
        <section id="code-project-1">
            <h2>⚙️ Code Project n°1: Embedded Software in the French Robotics Cup</h2>
            <p>In May 2026, I participated in the prestigious French Robotics Cup (Senior Category) as part of the INSA Rennes Robotics Club, securing a highly competitive 42nd place out of 121 teams[cite: 1].</p>
            <ul>
                <li><strong>Version Control:</strong> Implemented strict GitHub branching pipelines to merge real-time sensory node updates cleanly across a distributed multi-developer team[cite: 1].</li>
                <li><strong>Language Standard:</strong> Developed low-latency embedded algorithmic modules written entirely in C++ to achieve deterministic reactions during matches[cite: 1].</li>
                <li><strong>System Agility:</strong> Managed mission-critical software scripts under intense on-site pressure and tight scheduling blocks[cite: 1].</li>
            </ul>
        </section>

        <!-- CODE PROJECT 2 -->
        <section id="code-project-2">
            <h2>🔌 Code Project n°2: SCARA Robot Control Software rewrite</h2>
            <p>Building upon the theoretical foundations acquired during my fourth academic year in 2026, I coupled mathematical modeling with hardware verification by targeting high-speed pick-and-place robots[cite: 1].</p>

            <img class="project-img" src="https://images.unsplash.com/photo-1485827404703-89b55fcc595e?auto=format&fit=crop&w=800&q=80" alt="Industrial Robotic Testing">

            <ul>
                <li><strong>Mathematical Modeling:</strong> Completely rewrote the theoretical control and inverse kinematics software matrix for an industrial Stäubli SCARA robot using MATLAB[cite: 1].</li>
                <li><strong>Experimental Validation:</strong> Executed live physical loop testing on hardware, validating that the software script perfectly matched real-world trajectory profiles without boundary errors[cite: 1].</li>
                <li><strong>Toolchain Familiarity:</strong> Extended this robotics focus into self-taught system tools including ROS2, Docker containerization, and PyTorch deep-learning networks[cite: 1].</li>
            </ul>
        </section>

        <!-- AI PROJECT 1 -->
        <section id="ia-project-1">
            <h2>🧠 AI Project n°1: Neural Network Implementations for Autonomous Agents</h2>
            <p>My R&D work involves building reliable training configurations where neural policies can safely interact with simulated rigid-body physics engines before deployment.</p>
            <p>Below is a structural example of the policy network architectures utilized during my robotic reinforcement learning configurations inside NVIDIA Isaac Sim/Lab[cite: 1]:</p>
            
<pre><code>import torch
import torch.nn as nn

class RobotPolicyNetwork(nn.Module):
    """ Actor-Critic PPO network architecture for Duckiebot agent tracking """
    def __init__(self, state_dim, action_dim):
        super(RobotPolicyNetwork, self).__init__()
        self.actor = nn.Sequential(
            nn.Linear(state_dim, 128),
            nn.ReLU(),
            nn.Linear(128, 128),
            nn.ReLU(),
            nn.Linear(128, action_dim),
            nn.Tanh() # Continuous velocity outputs [-1, 1]
        )
        self.critic = nn.Sequential(
            nn.Linear(state_dim, 128),
            nn.ReLU(),
            nn.Linear(128, 64),
            nn.ReLU(),
            nn.Linear(64, 1)
        )

    def forward(self, state):
        value = self.critic(state)
        action_mean = self.actor(state)
        return action_mean, value

print("PPO Actor-Critic tracking structure initialized.")
</code></pre>
        </section>

        <!-- VOLUNTEERING SECTION -->
        <section id="volunteering">
            <h2>🤝 Leadership & Volunteering Highlights</h2>
            <p>Outside of pure code development, I actively invest energy into organizing academic events and testing my skills in global engineering ecosystems:</p>
            <ul>
                <li><strong>Corporate Communications Manager - Semaine Blanche GMA (Oct 2024 - Feb 2026):</strong> Co-organized a major corporate network tour for our entire engineering year group[cite: 1]. Managed funding campaigns and established corporate relations to secure site visits across 11 key technology facilities, including the CEA Tech laboratories in the Pays de la Loire region[cite: 1].</li>
                <li><strong>World Champion (Junior Category) - RoboCup (July 2021):</strong> Attained the ultimate global standing as Robotics World Champion at the international competition in Bangkok after a rigorous 2-year development cycle with the ElektronLibres public robotics club[cite: 1]. Proved an elite capability to work under immense pressure within collaborative English-speaking teams[cite: 1].</li>
            </ul>
        </section>
    </div>

</body>
</html>
