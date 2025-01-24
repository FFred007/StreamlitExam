# StreamlitExam
PS : La clé dans le fichier TOML a été désactivée, elle sert uniquement d'exemple ici 

## Groupe:
    * Zogbelemou Frederic
    * Benamara Amayas
    * FOAGOUO WABO Lemaire Junior

----------------- Etapes pour executer le projet sur son pc

    1. Récupérer le projet depuis GitHub
La première chose à faire est de télécharger ton projet. Pour cela, la personne doit aller sur ton dépôt GitHub et copier l'URL du dépôt (le lien HTTPS).

Ensuite, dans un terminal (ou un outil comme Git Bash sous Windows), elle doit taper cette commande :

bash
Copier
Modifier
git clone <URL_DU_DEPOT>
Exemple :
Si ton dépôt s’appelle StreamlitExam, la commande ressemblera à ceci :

bash
Copier
Modifier
git clone https://github.com/FFred007/StreamlitExam.git
Cela créera un dossier avec tous les fichiers de ton projet.

2. Se déplacer dans le dossier du projet
Une fois le projet téléchargé, il faut se rendre à l’intérieur du dossier pour travailler dessus. Par exemple, si le projet s’appelle StreamlitExam, la commande est :

bash
Copier
Modifier
cd StreamlitExam
Cela place la personne dans le dossier où sont tous les fichiers nécessaires.

3. Créer un environnement virtuel Python
Pour ne pas mélanger les dépendances de ton projet avec d’autres projets Python sur son ordinateur, il est recommandé de créer un environnement virtuel.

Créer l’environnement virtuel : La commande est la suivante :

bash
Copier
Modifier
python -m venv stenv
Cela va créer un dossier appelé stenv qui contiendra une version isolée de Python pour ton projet.

Activer l’environnement virtuel : Une fois l’environnement créé, il faut l’activer. La méthode dépend du système d’exploitation :

Sur Windows :

bash
Copier
Modifier
stenv\Scripts\activate
Sur Mac/Linux :

bash
Copier
Modifier
source stenv/bin/activate
Quand l’environnement est activé, le terminal montrera quelque chose comme (stenv) au début de chaque ligne, ce qui signifie qu’il utilise l’environnement virtuel.

4. Installer les dépendances
Dans ton projet, il doit y avoir un fichier nommé requirements.txt. Ce fichier liste tous les modules Python dont ton projet a besoin (comme streamlit ou openai).

Pour installer ces modules, il suffit de taper cette commande dans le terminal :

bash
Copier
Modifier
pip install -r requirements.txt
Cela téléchargera et installera tout ce dont le projet a besoin.

5. Configurer les clés API
Ton projet utilise probablement une clé d'API OpenAI pour fonctionner. Ces clés doivent être configurées dans un fichier spécial appelé secrets.toml, qui se trouve dans un dossier nommé .streamlit.

Voici ce que la personne doit faire :

Créer le fichier secrets.toml :
Si ce fichier n’existe pas encore, elle doit le créer manuellement dans un dossier .streamlit.
Si le dossier n’existe pas, elle peut le créer comme ceci :

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
Ensuite, elle doit créer le fichier secrets.toml dans ce dossier.

Ajouter la clé API dans le fichier :
Le contenu du fichier secrets.toml doit ressembler à ceci :

toml
Copier
Modifier
[OPENAI]
API_KEY = "sa_cle_api"
Il faut remplacer "sa_cle_api" par une vraie clé API OpenAI.

6. Lancer Streamlit
Une fois que tout est configuré, la personne peut lancer l'application Streamlit. La commande à taper est :

bash
Copier
Modifier
streamlit run chatbotgpt.py
chatbotgpt.py est le fichier principal de ton projet qui contient le code Streamlit. Si le fichier a un autre nom, elle devra adapter la commande en conséquence.
