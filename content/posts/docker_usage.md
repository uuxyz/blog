---
title: docker usage
date: 2023-09-18
---
Using Docker can make it more convenient to deploy your own applications or access pre-written programs by others. Below are some useful tips.

**Installation of Docker:**

On Manjaro, you can simply enter the following command:

```bash
sudo pacman -S docker
```

**Using Docker:**

Let's take WolframEngine as an example:

**Step 1:** Download the image from a proxy website:

shell

`docker pull dockerproxy.com/wolframresearch/wolframengine`

**Step 2:** Rename the image:

```bash
sudo docker tag dockerproxy.com/wolframresearch/wolframengine wolframresearch/wolframengine
```

**Step 3:** Remove the proxy image:

```bash
sudo docker rmi dockerproxy.com/wolframresearch/wolframengine
```

You can check the images you have with the `docker images` command.

**To enter the image:**

shell

```bash
sudo docker run wolframresearch/wolframengine
```

Using Docker provides a streamlined approach to deploying your applications or accessing pre-built ones. It simplifies the process, making it efficient for both personal and collaborative projects.