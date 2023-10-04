---
title: git usage
date: 2022-04-25
---
Mastering the use of Git can significantly enhance your work efficiency. Here are the steps to get started:

- **Install Git**: Firstly, you should install Git. Most Linux distributions come with Git pre-installed, so there's usually no need for additional installation. However, if you're using Manjaro, you can install Git with the following command:
```bash
sudo pacman -S git
```
- **Configure Your Personal Information**: Configure your personal information like your username and email, which will be associated with your Git commits. Replace "xyiii" and "[xyiii@pm.me](mailto:xyiii@pm.me)" with your own information.

```bash
git config --global user.name "xyiii"
git config --global user.email xyiii@pm.me
```

- **Specify a Text Editor (Optional)**: If you prefer a specific text editor, such as Emacs, you can set it as your default Git editor.

```bash
git config --global core.editor emacs
```

- **Set Up a Proxy (Optional)**: If you are in an area with network restrictions and need to use a proxy, you can configure Git to use a proxy server. Replace "[http://127.0.0.1:20172](http://127.0.0.1:20172)" with the actual proxy address.

```bash
git config --global http.proxy "http://127.0.0.1:20172"
```
- **Creating Your First Repository**: Now that you have Git set up, you can create your first Git repository. For example, to create a repository named "hello_world," use the following command:

```bash
git init hello_world
```

- **Cloning an Existing Repository**: Alternatively, you can clone an existing repository from a remote location. Replace the URL with the repository you want to clone.

```bash
git clone https://github.com/torvalds/linux.git
```

- **Making Changes and Committing**: Once you have a repository, you can make changes to the files and commit them. Here's how to stage changes, commit them, and push to a remote repository:

```bash
git add .
git commit -m "Add files via upload"
git push --all origin
```

- **Switching Branches**: Sometimes, you may need to switch between branches in your repository.

```bash
git switch gh-pages
```

- **Updating Your Repository**: To keep your local repository up-to-date with changes from the remote repository, use the following command:

```bash
git pull
```

By following these steps, you'll be well on your way to effectively using Git for your work.
We need to configure the gpg key in git to authenticate our commits.
```bash
git config --global user.signingkey CBE808B2A518258F9EA0B156E81B5EA1E5FF2F77
```

The following line of code sets up git to sign commits automatically.
```bash
git config --global commit.gpgsign true
```
