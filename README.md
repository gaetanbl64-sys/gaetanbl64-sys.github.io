<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaëtan Baylou-Lanot - Portfolio de Projets</title>
    <style>
        /* Design épuré inspiré du thème Chirpy de Samuel Neumann */
        :root {
            --bg-color: #ffffff;
            --text-color: #212529;
            --sidebar-bg: #f8f9fa;
            --sidebar-text: #495057;
            --accent-color: #2a7ae2;
            --code-bg: #f1f3f5;
            --border-color: #dee2e6;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            color: var(--text-color);
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
            display: flex;
            line-height: 1.6;
        }

        /* Barre latérale gauche */
        .sidebar {
            width: 300px;
            background-color: var(--sidebar-bg);
            border-right: 1px solid var(--border-color);
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            display: flex;
            flex-direction: column;
            padding: 2.5rem 1.2rem;
            box-sizing: border-box;
            overflow-y: auto; /* Permet de scroller dans le menu si la liste est longue */
        }

        .profile {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .profile-pic {
            width: 90px;
            height: 90px;
            background: #ced4da;
            border-radius: 50%;
            margin: 0 auto 1rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
        }

        .profile h1 {
            font-size: 1.2rem;
            margin: 0;
            color: #1a1a1a;
            line-height: 1.3;
        }

        .profile p {
            font-size: 0.85rem;
            color: #6c757d;
            margin: 0.5rem 0 0 0;
        }

        .nav-links {
            list-style: none;
            padding: 0;
            margin: 1rem 0 0 0;
        }

        .nav-links li {
            margin-bottom: 0.3rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--sidebar-text);
            font-weight: 500;
            font-size: 0.9rem;
            display: block;
            padding: 0.5rem 0.7rem;
            border-radius: 6px;
            transition: all 0.2s;
        }

        .nav-links a:hover {
            background-color: #e9ecef;
            color: var(--accent-color);
        }

        /* Zone de contenu principale */
        .content {
            margin-left: 300px;
            padding: 3.5rem;
            max-width: 850px;
            width: 100%;
            box-sizing: border-box;
        }

        .tag-container {
            margin-bottom: 0.5rem;
        }

        .tag {
            background: #e2e8f0;
            color: #4a5568;
            padding: 0.25rem 0.6rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-right: 0.5rem;
            text-transform: uppercase;
        }

        h1 { 
            font-size: 2.2rem; 
            color: #1a1a1a;
            margin: 0 0 0.5rem 0;
            line-height: 1.2;
        }

        .meta {
            font-size: 0.9rem;
            color: #6c757d;
            margin-bottom: 2.5rem;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 1rem;
        }

        h2 { 
            font-size: 1.5rem; 
            color: #1a1a1a;
            margin-top: 3rem; 
            border-bottom: 1px solid #f1f3f5;
            padding-bottom: 0.3rem;
        }

        p {
            margin: 1rem 0;
            color: #333;
        }

        ul {
            padding-left: 1.5rem;
        }

        li {
            margin-bottom: 0.5rem;
        }

        /* Blocs de code */
        pre {
            background-color: var(--code-bg);
            padding: 1.2rem;
            border-radius: 8px;
            overflow-x: auto;
            border: 1px solid var(--border-color);
            margin: 1.5rem 0;
        }

        code {
            font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
            font-size: 0.9rem;
            color: #d63384;
        }

        pre code {
            color: #212529;
        }

        blockquote {
            border-left: 4px solid var(--accent-color);
            margin: 1.5rem 0;
            padding: 0.5rem 1rem;
            background-color: #f8f9fa;
            color: #495057;
        }

        /* Mode Mobile Responsif */
        @media (max-width: 768px) {
            body { flex-direction: column; }
            .sidebar { width: 100%; height: auto; position: relative; border-right: none; border-bottom: 1px solid var(--border-color); padding: 1.5rem; }
            .content { margin-left: 0; padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <!-- BARRE LATÉRALE (SIDEBAR) -->
    <div class="sidebar">
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
            <li><a href="#my studies">🎓 My Studies: 3 Internships</a></li>
        </ul>
    </div>

    <!-- CONTENU PRINCIPAL -->
    <div class="content">
        <div class="tag-container">
            <span class="tag">robotics</span>
            <span class="tag">ai</span>
            <span class="tag">embedded</span>
            <span class="tag">engineering</span>
        </div>
        
        <h1>Détail de mes projets personnels & académiques</h1>
        <div class="meta">Mis à jour en 2026 • Par Gaëtan Baylou-Lanot</div>

        <!-- Section Introduction -->
        <section id="introduction">
            <h2>📌 Introduction</h2>
            <p>Bienvenue sur mon espace personnel de documentation. Ce site regroupe les différents projets sur lesquels j'ai travaillé, touchant à la fois à l'intelligence artificielle, au développement système, à la robotique et à des réalisations concrètes de conception.</p>
            <blockquote>
                <strong>Note aux recruteurs :</strong> Cette page me permet de détailler les aspects techniques et méthodologiques qui ne tiennent pas sur mon format de CV classique.
            </blockquote>
        </section>

        <!-- Section 1 : Van Conversion -->
        <section id="van-conversion">
            <h2>🚐 Van conversion: bref summary of my personality</h2>
            <p>[Décrivez ici brièvement votre projet d'aménagement de van. C'est une excellente façon de montrer votre autonomie, vos compétences en gestion de projet, en résolution de problèmes et en ingénierie concrète/bricolage].</p>
            <ul>
                <li>Conception des plans en 3D et optimisation de l'espace.</li>
                <li>Gestion du système électrique autonome (batteries, panneaux solaires).</li>
                <li>Choix des matériaux et isolation thermique.</li>
            </ul>
        </section>

        <!-- Section 3 : Code Projet n°1 -->
        <section id="code-project-1">
            <h2>⚙️ Code projet n°1: robotics' club in C++</h2>
            <p>[Détaillez ici votre contribution au club de robotique, notamment la partie développement bas niveau / système en C++].</p>
            <ul>
                <li>Développement orienté objet en C++ pour la gestion des actuateurs et capteurs.</li>
                <li>Optimisation du code pour des architectures embarquées à ressources limitées.</li>
                <li>Travail collaboratif en équipe via Git et méthodologie Agile.</li>
            </ul>
        </section>

        <!-- Section 4 : Code Project n°2 -->
        <section id="code-project-2">
            <h2>🔌 Code project n°2: robot control with ROS2</h2>
            <p>[Présentez ici vos compétences sur ROS2 (Robot Operating System), l'outil standard de l'industrie robotique].</p>
            <ul>
                <li>Création de nœuds (Nodes) ROS2 personnalisés en Python ou C++.</li>
                <li>Gestion des communications via les Topics, Services et Actions.</li>
                <li>Intégration et manipulation de données de capteurs (LiDAR, Caméra Odométrie).</li>
            </ul>
        </section>

        <!-- Section 5 : IA Project n°1 -->
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

        <!-- Section 2 : IA Project n°2 -->
        <section id="ia-project-2">
            <h2>🤖 IA project n°2: simulation and guidance of robot by RL</h2>
            <p>[Expliquez ici votre projet d'apprentissage par renforcement (Reinforcement Learning - RL) appliqué au guidage d'un robot en simulation].</p>
            <ul>
                <li>Définition de l'environnement de simulation (ex: OpenAI Gym, Webots, ou Gazebo).</li>
                <li>Modélisation de la fonction de récompense (reward function) pour l'évitement d'obstacles.</li>
                <li>Algorithmes testés : PPO, DQN ou DDPG.</li>
            </ul>
        </section>

        <!-- Section 6 :  Stages -->
        <section id="my studies">
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
