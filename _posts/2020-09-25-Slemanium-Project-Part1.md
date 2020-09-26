---
title: Project Slemanium Part 1
published: true
---

# [](#header-1) SLEMANIUM - PART 1

New cryptocurrency – Slemanium

Ini adalah projek yang saya buat untuk memahami konsep blockchain serta penerapanya dalam cryptocurrency. Project ini bernama SLEMANIUM ie. Sleman-ium. Saya menggunakan codebase dari bitcoin yang kemudian saya modifikasi.<br/><br/>

**Kriteria dari Slemanium**

| Nama Koin               | Slemanium                        |
|-------------------------|----------------------------------|
| Simbol Koin             | SLN                              |
| Block Time              | 2.5 Menit                        |
| Initial Block Reward    | 10                               |
| Halving Interval        | Setiap 10000 blok (174 hari)     |
| Port                    | RPC port : 19333 P2P port : 9333 |
| Total supply            | 2000000                          |
| difficulty readjustment | Setelah 576 blok                 |
| Block Size              | Up to 8 Mb                       |

<br/>

## Cloning Bitcoin

Clone bitcoin
```console
$ git clone -b 0.15 https://github.com/bitcoin/bitcoin.git slemanium && cd slemanium
```
Remove old git 
```console
$ rm -­rf .git
```
Initialize new git
```console
$ git init
$ git add ­-A 
$ git commit -m "initial commit"
```
Add remote repository

```console
$ git remote add origin https://github.com/[PATH TO YOUR REPOSITORY].git
```
Push to remote repository
```console
$ git push -f origin master
```
<br>

## Rebranding

In slemanium directory run

```console
$ find . -exec rename 's/bitcoin/slemanium/' {} ";"
$ find . -exec rename 's/btc/sln/' {} ";"
```
Note : If you encounter error with rename, install it first

`$ sudo apt-get install rename -y`

Create bash script file and copy this command 
```console
$ find ./ -type f -readable -writable -exec sed -i "s/bitcoin/slemanium/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/Bitcoin/Slemanium/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/BitCoin/SlemaNium/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/BITCOIN/SLEMANIUM/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/bitcoind/slemaniumd/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/BTC/SLN/g" {} ";"
$ find ./ -type f -readable -writable -exec sed -i "s/btc/sln/g" {} ";"
```
This change will effect git, use this command to avoid git's bad index file signature error:
```console
$ rm -f .git/index
$ git reset
$ git add -A
$ git commit -m "rename bitcoin into slemanium occurrences"
$ git push origin master
```

**END** of this part