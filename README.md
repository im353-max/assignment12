GitHub Actions
<img width="3815" height="1285" alt="GitHubActions" src="https://github.com/user-attachments/assets/51a86b35-4d70-445f-9cd6-b7cd0b90b20f" />
https://github.com/im353-max/assignment12/actions

DockerHub
<img width="3797" height="1780" alt="Dockerhub" src="https://github.com/user-attachments/assets/ceaf81e3-56f0-4f08-8e56-356b1754cbba" />
https://hub.docker.com/repository/docker/imanayath/601_module12/general

/health Read Health
<img width="2137" height="1750" alt="GetHealth" src="https://github.com/user-attachments/assets/7ee29c82-f08f-4759-bd6c-d42bc9eed759" />

/auth/register Register
<img width="2075" height="1785" alt="RegisterAuth" src="https://github.com/user-attachments/assets/f09a77bc-9296-44f2-b5c3-b7f313423af0" />

/auth/login Login Json
<img width="1895" height="1807" alt="LoginAuth" src="https://github.com/user-attachments/assets/6701d558-ffaf-458e-bcb4-02ccf8892f13" />

/auth/token Login From
<img width="1605" height="1805" alt="AuthToken" src="https://github.com/user-attachments/assets/3373996f-23fd-4366-8816-2c31fb4d5061" />

/calculations List Calculations
<img width="1555" height="1802" alt="Calculations" src="https://github.com/user-attachments/assets/e3b82743-4d6d-4132-baef-51bb07e48f50" />

/calculations Create Calculation
<img width="1560" height="1760" alt="CreateCalculation" src="https://github.com/user-attachments/assets/f5e88e33-b15f-40c7-9307-bf8bb0397de7" />

/calculations/{calc_id} Get Calculation
<img width="1552" height="1625" alt="GetCalculation" src="https://github.com/user-attachments/assets/e7e283ca-4ade-40e3-95c6-28674fa9e203" />

/calculations/{calc_id} Update Calculation
<img width="1582" height="1787" alt="UpdateCalculation" src="https://github.com/user-attachments/assets/4314a8ca-d393-42e7-8e57-e7e44f68b60e" />

/calculations/{calc_id} Delete Calculation
<img width="1572" height="1570" alt="DeleteCalculation" src="https://github.com/user-attachments/assets/46e8fb35-9bce-494b-ac31-6d4a4e0ac160" />



# 📦 Project Setup

---

# 🧩 1. Install Homebrew (Mac Only)

> Skip this step if you're on Windows.

Homebrew is a package manager for macOS.  
You’ll use it to easily install Git, Python, Docker, etc.

**Install Homebrew:**

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**Verify Homebrew:**

```bash
brew --version
```

If you see a version number, you're good to go.

---

# 🧩 2. Install and Configure Git

## Install Git

- **MacOS (using Homebrew)**

```bash
brew install git
```

- **Windows**

Download and install [Git for Windows](https://git-scm.com/download/win).  
Accept the default options during installation.

**Verify Git:**

```bash
git --version
```

---

## Configure Git Globals

Set your name and email so Git tracks your commits properly:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

Confirm the settings:

```bash
git config --list
```

---

## Generate SSH Keys and Connect to GitHub

> Only do this once per machine.

1. Generate a new SSH key:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

(Press Enter at all prompts.)

2. Start the SSH agent:

```bash
eval "$(ssh-agent -s)"
```

3. Add the SSH private key to the agent:

```bash
ssh-add ~/.ssh/id_ed25519
```

4. Copy your SSH public key:

- **Mac/Linux:**

```bash
cat ~/.ssh/id_ed25519.pub | pbcopy
```

- **Windows (Git Bash):**

```bash
cat ~/.ssh/id_ed25519.pub | clip
```

5. Add the key to your GitHub account:
   - Go to [GitHub SSH Settings](https://github.com/settings/keys)
   - Click **New SSH Key**, paste the key, save.

6. Test the connection:

```bash
ssh -T git@github.com
```

You should see a success message.

---

# 🧩 3. Clone the Repository

Now you can safely clone the course project:

```bash
git clone <repository-url>
cd <repository-directory>
```

---

# 🛠️ 4. Install Python 3.10+

## Install Python

- **MacOS (Homebrew)**

```bash
brew install python
```

- **Windows**

Download and install [Python for Windows](https://www.python.org/downloads/).  
✅ Make sure you **check the box** `Add Python to PATH` during setup.

**Verify Python:**

```bash
python3 --version
```
or
```bash
python --version
```

---

## Create and Activate a Virtual Environment

(Optional but recommended)

```bash
python3 -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate.bat  # Windows
```

### Install Required Packages

```bash
pip install -r requirements.txt
```

---

# 🐳 5. (Optional) Docker Setup

> Skip if Docker isn't used in this module.

## Install Docker

- [Install Docker Desktop for Mac](https://www.docker.com/products/docker-desktop/)
- [Install Docker Desktop for Windows](https://www.docker.com/products/docker-desktop/)

## Build Docker Image

```bash
docker build -t <image-name> .
```

## Run Docker Container

```bash
docker run -it --rm <image-name>
```

---

# 🚀 6. Running the Project

- **Without Docker**:

```bash
python main.py
```

(or update this if the main script is different.)

- **With Docker**:

```bash
docker run -it --rm <image-name>
```

---

# 📝 7. Submission Instructions

After finishing your work:

```bash
git add .
git commit -m "Complete Module X"
git push origin main
```

Then submit the GitHub repository link as instructed.

---

# 🔥 Useful Commands Cheat Sheet

| Action                         | Command                                          |
| ------------------------------- | ------------------------------------------------ |
| Install Homebrew (Mac)          | `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` |
| Install Git                     | `brew install git` or Git for Windows installer |
| Configure Git Global Username  | `git config --global user.name "Your Name"`      |
| Configure Git Global Email     | `git config --global user.email "you@example.com"` |
| Clone Repository                | `git clone <repo-url>`                          |
| Create Virtual Environment     | `python3 -m venv venv`                           |
| Activate Virtual Environment   | `source venv/bin/activate` / `venv\Scripts\activate.bat` |
| Install Python Packages        | `pip install -r requirements.txt`               |
| Build Docker Image              | `docker build -t <image-name> .`                |
| Run Docker Container            | `docker run -it --rm <image-name>`               |
| Push Code to GitHub             | `git add . && git commit -m "message" && git push` |

---

# 📋 Notes

- Install **Homebrew** first on Mac.
- Install and configure **Git** and **SSH** before cloning.
- Use **Python 3.10+** and **virtual environments** for Python projects.
- **Docker** is optional depending on the project.

---

# 📎 Quick Links

- [Homebrew](https://brew.sh/)
- [Git Downloads](https://git-scm.com/downloads)
- [Python Downloads](https://www.python.org/downloads/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [GitHub SSH Setup Guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
