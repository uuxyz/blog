---
title: gpg usage
date: 2022-05-07
---
## generate
First we need to generate a key.
```bash
gpg --full-generate-key
```

## import
If you already have a private key, then you can import it and change its trust level to ultimate.
```bash
gpg --import u_prv.gpg
gpg --edit-key u_u_u
trust
  1 = I don't know or won't say
  2 = I do NOT trust
  3 = I trust marginally
  4 = I trust fully
  5 = I trust ultimately
  m = back to the main menu
5
save
```

## encrypt and decrypt
We can encrypt the file with our public key.
```bash
gpg -r u_u_u -ae hello_world.txt -o hello_world.gpg
```
Then decrypt it with the private key.
```bash
gpg -d hello_world.gpg -o out.txt
```

## signature
We can use our private key to sign a file, the first method generates a standalone signature file, the second method deposits the contents of the file along with the signature, and the third method, which applies to text, generates an `.asc` text containing the original message and additional signatures.
```bash
gpg -b hello_world.txt
gpg -s hello_world.txt
gpg --clearsign hello_world.txt
```

Accordingly, we can verify these signatures. The first three ways correspond to the three signature methods mentioned above. If you only need to verify and not output the encrypted information, then you can use the `--verify` option
```bash
gpg -d hello_world.txt hello_world.txt.sig
gpg -d hello_world.txt.gpg
gpg -d hello_world.txt.asc
gpg --verify hello_world.txt.gpg
```

Export and keep your keys safe
```bash
gpg --export -a u_u_u -o u_pub.gpg 
gpg --export -a u_u_u -o u_prv.gpg 
```

## ssh
You can use gpg to manage ssh logins.
Enable gpg-agent first.
```bash
echo "enable-ssh-support" >> ~/.gnupg/gpg-agent.conf
```
Find the subkey you need. Then add it to the `sshcontrol` file
```bash
gpg --list-keys --with-keygrip
echo "4B819AB5710A8EC4DF1B9E2169B9147975778499" ~/.gnupg/sshcontrol
```
Start gpg-agent.
```bash
gpgconf --launch gpg-agent
export SSH_AUTH_SOCK=$(gpgconf --list-dirs agent-ssh-socket)
```
Then you can export your ssh public key.
```bash
ssh-add -L
ssh-add -l
```
Connect to github and test it.
```bash
ssh -T git@github.com:uuxyz/history.git
```

If it goes well, you'll see this:
> Hi uuxyz! You've successfully authenticated, but GitHub does not provide shell access.