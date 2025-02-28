# **📦 Cahier des Charges – Mini-Projet : Prototype de Mouvements pour *Gaïa’s Guardian***  

📢 **Objectif du projet**  
Ce mini-projet a pour but de mettre en place **une base solide pour le gameplay de *Gaïa’s Guardian***. L’objectif est d’implémenter **un prototype fonctionnel** avec les **mécaniques de déplacement et de contrôle du personnage** dans Unity.  

🛠 **Technologies utilisées**  
✅ **Unity 2022+ (2D Core Template)**  
✅ **Langage : C#**  
✅ **Versionnage : GitHub (optionnel)**  

---

## **📂 1. Structure du Projet Unity**  

📌 **Le projet doit suivre une organisation claire**, facilitant la lecture et la maintenance. Voici l’arborescence des fichiers attendue :  

```
📁 GaiaGuardian_Prototype
│── 📁 Assets
│   │── 📁 Animations
│   │   ├── Player_Idle.anim
│   │   ├── Player_Run.anim
│   │   ├── Player_Jump.anim
│   │   ├── Player_Dash.anim
│   │── 📁 Materials
│   │── 📁 Prefabs
│   │   ├── Player.prefab
│   │   ├── Platform.prefab
│   │── 📁 Scenes
│   │   ├── MainScene.unity
│   │── 📁 Scripts
│   │   ├── Player
│   │   │   ├── PlayerMovement.cs
│   │   │   ├── PlayerJump.cs
│   │   │   ├── PlayerDash.cs
│   │   ├── Camera
│   │   │   ├── CameraFollow.cs
│   │   ├── Environment
│   │   │   ├── Platform.cs
│   │── 📁 Sprites
│   │   ├── Player_Idle.png
│   │   ├── Player_Run.png
│   │   ├── Player_Jump.png
│   │   ├── Player_Dash.png
│   │── 📁 UI
│── 📁 Packages
│── 📁 ProjectSettings
│── 📁 Logs (optionnel)
│── README.md
│── .gitignore
│── GaiaGuardian_Prototype.sln
```

---

## **🎮 2. Fonctionnalités Attenues**  

### **🕹️ 2.1 Déplacements du Joueur**  

✅ **Déplacement gauche/droite**  
- Le joueur doit pouvoir **se déplacer à gauche et à droite** de manière fluide.  
- Une accélération/décélération progressive est attendue.  

✅ **Saut & Double Saut**  
- Le joueur doit pouvoir **sauter** et **effectuer un double saut**.  
- La détection du sol est essentielle pour empêcher un saut infini.  
- Le saut doit être influencé par la gravité et la pression sur la touche.  

✅ **Dash aérien**  
- Un **dash directionnel** doit être disponible pour une courte propulsion en l’air.  
- Une **limitation de son usage** doit être implémentée pour éviter le spam.  
- Une **animation et un effet visuel doivent accompagner** le dash.  

✅ **Arrêt précis & inertie**  
- Lorsqu’un joueur relâche une touche de déplacement, le personnage **ne doit pas s’arrêter brutalement**, sauf en cas de dash.  

---

### **📷 2.2 Caméra Dynamique**  

✅ **Suivi du joueur**  
- La caméra doit **suivre le joueur** tout en appliquant un effet de **lissage** (*lerping*).  

✅ **Zone de tolérance**  
- La caméra ne doit pas être **trop rigide** : prévoir une **zone de tolérance** où le joueur peut bouger sans que la caméra ne le suive immédiatement.  

✅ **Focus dynamique** (Optionnel)  
- Lors du **dash ou d’un saut important**, la caméra peut **légèrement anticiper** le mouvement pour donner plus de visibilité au joueur.  

---

### **🌍 2.3 Environnement et Collisions**  

✅ **Plateformes statiques**  
- Les plateformes doivent être des **objets solides** détectables par le joueur.  
- Les plateformes doivent être instanciables via **des prefabs**.  

✅ **Plateformes mobiles (optionnel)**  
- Des plateformes qui **se déplacent horizontalement ou verticalement** peuvent être ajoutées.  

✅ **Gestion des collisions**  
- Le joueur ne doit pas pouvoir **traverser les plateformes** ou **rester bloqué dans un mur**.  

---

### **🎨 2.4 Animations et Effets Visuels**  

✅ **Animations du personnage**  
- Une animation doit être **associée à chaque action** :  
  - **Idle (statique)**  
  - **Run (course)**  
  - **Jump (saut en l’air)**  
  - **Dash (propulsion rapide)**  

✅ **Effet visuel sur le dash**  
- Un effet de **traînée lumineuse** doit être visible lors du dash.  

✅ **Feedback visuel des actions**  
- L’utilisation d’un **léger effet de squash/stretch** sur le saut est encouragée.  

---

### **💾 2.5 Système de Contrôles**  

✅ **Mapping des touches attendu**  
| **Action** | **Clavier** | **Manette** |
|-----------|-----------|-----------|
| Déplacement | ← / → (A/D) | Joystick gauche |
| Saut | Espace | Bouton A |
| Dash | Shift | Bouton X |
| Pause (optionnel) | Échap | Start |

---

## **📢 3. Contraintes Techniques**  

📌 **Code clair et bien structuré**  
- Séparer les scripts **PlayerMovement, PlayerJump et PlayerDash** au lieu d’un seul gros script.  
- Nommer clairement les variables et fonctions.  

📌 **Optimisation & Performances**  
- **Limiter les appels à `Update()`** en favorisant **les événements et les coroutines**.  
- **Éviter les rigidbody inutiles** sur les objets statiques.  

📌 **Versionnage du projet**  
- Optionnel mais encouragé : **utilisation de Git et GitHub**.  

---

## **✅ 4. Objectifs du Mini-Projet**  

À la fin de ce mini-projet, vous devrez avoir :  
✅ Un **personnage jouable avec un mouvement fluide**.  
✅ Une **caméra dynamique qui suit le joueur**.  
✅ Un système de **saut/double saut/dash bien implémenté**.  
✅ Une gestion propre des **plateformes et des collisions**.  
✅ Des **animations et effets visuels immersifs**.  

📢 **Ce prototype servira de base pour le projet *Gaïa’s Guardian*.**  

---

## **📂 5. Fichiers et Livrables Attendus**  

✅ **Projet Unity complet** organisé selon la structure ci-dessus.  
✅ **README.md** avec un récapitulatif du projet et des instructions d’installation.  
✅ **Brève vidéo de démonstration du gameplay (optionnel).**  

---

## **📌 6. Ressources Utiles**  

📖 **[Documentation Unity - Mouvements](https://docs.unity3d.com/Manual/)**  
📖 **[Gestion de la caméra en 2D](https://docs.unity3d.com/Manual/CameraUsage.html)**  
📖 **[Brackeys - Plateformer Unity](https://www.youtube.com/watch?v=K1xZ-rycYY8)**  
📖 **[GitHub - Guide d’initiation](https://git-scm.com/book/en/v2)**  
