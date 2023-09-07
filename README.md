# Website IDE (website-ide)

Docker Compose configuration file for setup of the website integrated development environment (IDE)

## Details

Setup configuration for a [Docker](https://www.docker.com/) self-hosted [(linuxserver) code server](https://hub.docker.com/r/linuxserver/code-server) image enabling the creation and development of a [Hugo](https://gohugo.io/) static site.  The site scaffolding is generated in a hosted volume by the [(klakegg) hugo](https://hub.docker.com/r/klakegg/hugo) image with a live server instance of the [(klakegg) hugo](https://hub.docker.com/r/klakegg/hugo) image providing continual output of the rendered site.

## SSH Keygen

Upon accessing the code server, use the integrated terminal to create new SSH keys for this instance in it's configuration location:

```
ssh-keygen -t ed25519 -C "your_email@example.com" -f ../.ssh/github
```

Once generated, copy the contents of the public key (`../.ssh/github.pub`) and add them to your [GitHub](https://github.com/) account.

## Git Credentials

In the code server terminal, issue the following commands to setup [Git](https://git-scm.com/) credentials to prepare the environment for commands that will interact with the repository.

Set the username: 

```
git config --global user.name "username"
```

Set the email address:

```
git config --global user.email "email address"
```

## Versioning

* 1.0
    * [(linuxserver) code server](https://hub.docker.com/r/linuxserver/code-server): [4.16.1](https://hub.docker.com/layers/linuxserver/code-server/4.16.1/images/sha256-b7c3cd753e7d65e58e110af626494ba654f5f85235000cded7f3240a5671e323?context=explore)
    * [(klakegg) hugo](https://hub.docker.com/r/klakegg/hugo): [0.111.3](https://hub.docker.com/layers/klakegg/hugo/0.111.3/images/sha256-c3ef780efb22fe5932895133b228b72f4acd2a1b83ff36dca4b984da6850fb00?context=explore)

*[IDE]: Integrated Development Environment

*[SSH]: Secure shell
