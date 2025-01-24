
Instructions pour lancer le projet Streamlit depuis GitHub
Récupérer le projet depuis GitHub

Copiez l’URL du dépôt GitHub.
Ouvrez un terminal et tapez la commande suivante pour cloner le projet :
bash
Copier
Modifier
git clone <URL_DU_DEPOT>
Exemple :
bash
Copier
Modifier
git clone https://github.com/FFred007/StreamlitExam.git
Entrez dans le dossier cloné avec :
bash
Copier
Modifier
cd StreamlitExam
Créer un environnement virtuel Python

Créez un environnement virtuel nommé stenv :
bash
Copier
Modifier
python -m venv stenv
Activez l’environnement virtuel :
Sous Windows :
bash
Copier
Modifier
stenv\Scripts\activate
Sous Mac/Linux :
bash
Copier
Modifier
source stenv/bin/activate
Installer les dépendances

Installez les modules nécessaires en utilisant le fichier requirements.txt :
bash
Copier
Modifier
pip install -r requirements.txt
Configurer les clés API

Créez un dossier .streamlit dans le répertoire du projet :
Sous Windows :
bash
Copier
Modifier
mkdir .streamlit
Sous Mac/Linux :
bash
Copier
Modifier
mkdir -p .streamlit
Dans ce dossier, créez un fichier secrets.toml :
Sous Windows :
bash
Copier
Modifier
echo > .streamlit\secrets.toml
Sous Mac/Linux :
bash
Copier
Modifier
touch .streamlit/secrets.toml
Ouvrez le fichier secrets.toml et ajoutez-y votre clé API OpenAI :
toml
Copier
Modifier
[OPENAI]
API_KEY = "votre_clé_api_openai"
Lancer l’application Streamlit

Exécutez la commande suivante pour démarrer l’application :
bash
Copier
Modifier
streamlit run chatbotgpt.py
Une fenêtre du navigateur s’ouvrira avec l’interface utilisateur du chatbot.
