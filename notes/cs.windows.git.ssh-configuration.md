---
id: v1fvebmjnow6fymca4xpcbq
title: SSH Configuration
desc: ''
updated: 1708434173373
created: 1708428820389
---

### Prerequisites :
- Install [[cs.windows.git]]
- Add your `user.name` and `user.email` in `git config --global`

## Best Way

- Reference : https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/GitHub-SSH-Windows-Example
- No need for `ssh-agent`

Open Windows Terminal (No admin privileges required)

### 1. Genereate the key

```powershell
ssh-keygen -o -t rsa -C "himanshugoswami.12feb@gmail.com"
```

### 2. In your `~/.ssh` in windows
Look for these 2 files : `id_rsa` and `id_rsa.pub`

Copy the `.pub` file and paste it into Github

---

## Github Article Way (Bad-Way)

Do these steps in git bash  
- Git Bash is a commonly used tool on Windows for Git-related operations and provides compatibility with the majority of Git commands and workflows.

> Imp :
> > ssh-agent will cause a problem in windows. You can solve it by simply using git bash and adding ssh-keys to ssh-agent from it

### 1. Generate SSH Keys

Instructions given on github

### 2. Adding SSH Keys to ssh-agent

#### 2.1 In windows

> Imp : To install the SSH Agent on windows you need administator permissions to open **powershell as administrator**

#### 2.2 Using `git bash`

```bash
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```

This `id_rsa` is your private key

### 3. Pasting SSH Keys to Github

You'll be pasting your public key


Now if you clone from git bash it'll work perfectly but from windows it won't due to ssh-agent problem