<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaëtan Baylou-Lanot - Portfolio de Projets</title>
    <style>
        /* ==========================================================================
           DIRECTIONS ARTISTIQUE : INSPIRATION CHIRPY (MINIMALISTE & LAB)
           ========================================================================== */
        :root {
            --bg-color: #ffffff;
            --text-color: #343a40;
            --heading-color: #1c1f23;
            --sidebar-bg: #fbfbfb;
            --sidebar-text: #5c6266;
            --accent-color: #007bff;
            --accent-bg-light: #e3f2fd;
            --code-bg: #1e1e1e;
            --code-text: #f8f8f2;
            --border-color: #eaeaea;
            --tag-bg: #eff1f3;
            --tag-text: #6c757d;
        }

        body {
            font-family: "-apple-system", BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            color: var(--text-color);
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            /* Flex supprimé ici pour bloquer la structure proprement */
            -webkit-font-smoothing: antialiased;
        }

        /* BARRE LATÉRALE GAUCHE */
        .sidebar {
            width: 260px; /* Légèrement plus fine pour gagner de l'espace */
            background-color: var(--sidebar-bg);
            border-right: 1px solid var(--border-color);
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 3rem 1.5rem 1.5rem 1.5rem;
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
            width: 75px;
            height: 75px;
            background: linear-gradient(135deg, #e0e0e0, #f5f5f5);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            margin-bottom: 1.2rem;
            box-shadow: inset 0 2px 4px rgba(0,0,0,0.05);
        }

        .profile h1 {
            font-size: 1.25rem;
            font-weight: 700;
            margin: 0;
            color: var(--heading-color);
            letter-spacing: -0.025em;
        }

        .profile p {
            font-size: 0.85rem;
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
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 0.55rem 0.7rem;
            border-radius: 6px;
            transition: all 0.15s ease-in-out;
        }

        .nav-links a:hover {
            background-color: #f1f3f5;
            color: var(--heading-color);
        }

        .sidebar-footer {
            display: flex;
            gap: 15px;
            padding-left: 0.7rem;
            font-size: 0.9rem;
            color: #adb5bd;
        }
        
        .sidebar-footer a {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.2s;
        }
        .sidebar-footer a:hover { color: var(--heading-color); }

        /* ZONE DE CONTENU PRINCIPALE (CORRIGÉE) */
        .content {
            margin-left: 260px; /* Colle pile au 260px de la sidebar */
            padding: 3rem 2rem 3rem 1.5rem; /* 1.5rem à gauche = le texte est juste à côté de la ligne */
            max-width: 800px; /* Limite la largeur de lecture pour le style Chirpy */
            box-sizing: border-box;
        }

        /* Tags discrets style Chirpy */
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
            font-size: 2.4rem; 
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
        }

        ul {
            padding-left: 1.25rem;
            margin: 1rem 0;
        }

        li {
            margin-bottom: 0.6rem;
            color: var(--text-color);
        }
        
        li strong {
            color: var(--heading-color);
        }

        /* BANDEAU D'ALERTE STYLE CHIRPY PROMPT-INFO */
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

        /* BLOCS DE CODE STYLE IDE SOMBRE */
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

        /* ASSURANCE QUALITÉ RESPONSIVE */
        @media (max-width: 850px) {
            .sidebar { width: 100%; height: auto; position: relative; padding: 2rem 1.5rem; border-right: none; border-bottom: 1px solid var(--border-color); }
            .content { margin-left: 0; padding: 2.5rem 1.5rem; }
        }
    </style>
</head>
<body>

    <div class="sidebar">
        <div class="sidebar-top">
            <div class="profile">
                <div class="profile-pic">🚀</div>
                <h1>Gaëtan Baylou-Lanot</h1>
                <p>Mon Portfolio de Projets</p>
            </div>
            <ul class="nav-links">
                <li><a href="#introduction">📌 Introduction</a></li>
                <li><a href="#van-conversion">🚐 Van Conversion</a></li>
                <li><a href="#code-project-1">⚙️ Code Projet n°1 (C++)</a></li>
                <li><a href="#code-project-2">🔌 Code Project n°2 (ROS2)</a></li>
                <li><a href="#ia-project-1">🧠 IA Project n°1 (ML)</a></li>
                <li><a href="#ia-project-2">🤖 IA Project n°2 (RL)</a></li>
                <li><a href="#my-studies">🎓 My Studies: 3 Internships</a></li>
            </ul>
        </div>
        
        <div class="sidebar-footer">
            <a href="#" title="GitHub">🐙</a>
            <a href="#" title="Mail">✉️</a>
            <a href="#" title="CV">📄</a>
        </div>
    </div>

    <div class="content">
        <div class="tag-container">
            <span class="tag">robotics</span>
            <span class="tag">ai</span>
            <span class="tag">embedded</span>
            <span class="tag">engineering</span>
        </div>
        
        <h1 class="main-title">Détail de mes projets personnels & académiques</h1>
        <div class="meta">
            <span>Mis à jour en 2026</span>
            <span>•</span>
            <span>Par Gaëtan Baylou-Lanot</span>
        </div>

        <section id="introduction">
            <h2>📌 Introduction</h2>
            <p>Bienvenue sur mon espace personnel de documentation. Ce site regroupe les différents projets sur lesquels j'ai travaillé, touchant à la fois à l'intelligence artificielle, au développement système, à la robotique et à des réalisations concrètes de conception.</p>
            
            <blockquote class="prompt-info">
                <span><strong>Note aux recruteurs :</strong> Cette page me permet de détailler les aspects techniques et méthodologiques qui ne tiennent pas sur mon format de CV classique.</span>
            </blockquote>
        </section>

        <section id="van-conversion">
            <h2>🚐 Van conversion: bref summary of my personality</h2>
            <p>[Décrivez ici brièvement votre projet d'aménagement de van. C'est une excellente façon de montrer votre autonomie, vos compétences en gestion de projet, en résolution de problèmes et en ingénierie concrète/bricolage].</p>
            <ul>
                <li><strong>Conception :</strong> Plans en 3D et optimisation fine de l'espace.</li>
                <li><strong>Énergie :</strong> Gestion du système électrique autonome (batteries lithium, panneaux solaires).</li>
                <li><strong>Structure :</strong> Choix des matériaux légers et isolation thermique multicouche.</li>
            </ul>
        </section>

        <section id="code-project-1">
            <h2>⚙️ Code projet n°1: robotics' club in C++</h2>
            <p>[Détaillez ici votre contribution au club de robotique, notamment la partie développement bas niveau / système en C++].</p>
            <ul>
                <li>Développement orienté objet en C++ pour la gestion des actuateurs et capteurs.</li>
                <li>Optimisation du code pour des architectures embarquées à ressources limitées.</li>
                <li>Travail collaboratif en équipe via Git et méthodologie Agile.</li>
            </ul>
        </section>

        <section id="code-project-2">
            <h2>🔌 Code project n°2: robot control with ROS2</h2>
            <p>[Présentez ici vos compétences sur ROS2 (Robot Operating System), l'outil standard de l'industrie robotique].</p>
            <ul>
                <li>Création de nœuds (Nodes) ROS2 personnalisés en Python ou C++.</li>
                <li>Gestion des communications via les Topics, Services et Actions.</li>
                <li>Intégration et manipulation de données de capteurs (LiDAR, Caméra Odométrie).</li>
            </ul>
        </section>

        <section id="ia-project-1">
            <h2>🧠 IA project n°1: deployment of a supervised learning of food</h2>
            <p>[Présentez votre projet d'apprentissage supervisé dédié à la reconnaissance ou classification de nourriture].</p>
            <p>Voici un aperçu de l'architecture ou du pipeline de traitement utilisé pour ce modèle :</p>
            
<pre><code>import tensorflow as tf
from tensorflow.keras import layers, models

def create_food_model(input_shape, num_classes):
    """ Création d'un réseau de neurones convolutif (CNN) pour la classification """
    model = models.Sequential([
        layers.Conv2D(32, (3, 3), activation='relu', input_shape=input_shape),
        layers.MaxPooling2D((2, 2)),
        layers.Conv2D(64, (3, 3), activation='relu'),
        layers.MaxPooling2D((2, 2)),
        layers.Flatten(),
        layers.Dense(64, activation='relu'),
        layers.Dense(num_classes, activation='softmax')
    ])
    return model

print("Structure de l'algorithme d'apprentissage supervisé initialisée.")
</code></pre>
        </section>

        <section id="ia-project-2">
            <h2>🤖 IA project n°2: simulation and guidance of robot by RL</h2>
            <p>[Expliquez ici votre projet d'apprentissage par renforcement (Reinforcement Learning - RL) appliqué au guidage d'un robot en simulation].</p>
            <ul>
                <li>Définition de l'environnement de simulation (ex: OpenAI Gym, Webots, ou Gazebo).</li>
                <li>Modélisation de la fonction de récompense (reward function) pour l'évitement d'obstacles.</li>
                <li>Algorithmes testés : PPO, DQN ou DDPG.</li>
            </ul>
        </section>

        <section id="my-studies">
            <h2>🎓 My studies: 3 internships</h2>
            <p>[Utilisez cette conclusion pour lier vos projets personnels avec vos expériences professionnelles de stage et votre parcours d'études].</p>
            <ul>
                <li><strong>Stage n°1 :</strong> [Intitulé du poste / Entreprise] — Focus sur [Techno clé].</li>
                <li><strong>Stage n°2 :</strong> [Intitulé du poste / Entreprise] — Focus sur [Techno clé].</li>
                <li><strong>Stage n°3 :</strong> [Intitulé du poste / Entreprise] — Focus sur [Techno clé].</li>
            </ul>
        </section>
    </div>

</body>
</html>
