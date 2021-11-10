# Building a messaging app on Solana: Starting with a blockchain time capsule

Welcome to the Solana messaging app quest. With this quest you'll get upto speed with the most rapidly rising blockchain in the market: *Solana*. It would be awesome if you know a bit 
of Rust or C++ already and are familiar with how blockchains work, but even if you do not have any specific background of Rust or Solana development, we will have all bases covered. If 
you have a high level of interest and motivation, we should be good to go ahead.

In this quest, we will be developing a blockchain based time-capsule. This essentially means that you'll be able to leave a message on the Solana blockchain and anyone can view it for as
long as the Solana blockchain itself exists. Your message will survive the test of time and could not be taken down by anyone. 

This time-capsule quest will set us up for extending this project and creating an entire messaging app. How cool is that, right?

## Setting up the Environment: 

This quest could get a little cumbersome, but stick till the end and you'll thank yourself for that ;)

### Node.js

Node.js can be easily installed from [this page](https://nodejs.org/en/download/), however, we would advise using [nvm](https://github.com/nvm-sh/nvm) for downloading and managing your node versions.

### Solana Tool Suite

Solana Tool Suite is a really smooth CLI developer tooling from Solana labs and can be downloaded from [here](https://docs.solana.com/cli/install-solana-cli-tools). Note that if you are using a Windows system, the `solana-test-validator` command might not
work on your system.

### Anchor

[https://project-serum.github.io/anchor/getting-started/introduction.html]

Since Solana is still a pretty new blockchain compared to the establised ones out there, it's developer tooling too is pretty limited and cumbersome as of now. However, it is rapidly improving 
and it does so on a daily basis. At the forefront of this development is Anchor, by [Armani Ferrante](https://twitter.com/armaniferrante). You can think of it like the Ruby on Rails framework for
Ruby, that means yes, you can develop things on vanilla Ruby, but Ruby on Rails makes your life much much easier, right? That's the same with Anchor and Solana development. Anchor is the Hardhat of 
Solana development plus much more. It offers a Rust DSL (basically, an easier Rust) to work with along with IDL, CLI and workspace management. 

#### Installation:

Installing Anchor should be straight-forward if you follow the instructions given [here](https://project-serum.github.io/anchor/getting-started/installation.html)

**Fair Warning** : If you are using a Windows system, we highly suggest using [WSL2](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux) (Windows sub-system for Linux) or switching to a Linux environment. Setting up WSL is also quick and easy. A 
good walk-through can be found [here](https://www.youtube.com/watch?v=X3bPWl9Z2D0&ab_channel=BeachcastsProgrammingVideos)

### Phantom Wallet:

Follow the instructions over at the [Phantom website](https://phantom.app/) to download a browser that will help us interact with our Solana programs.

## Running configurations on Solana CLI

The first command you should run on your terminal (assuming Solana CLI was properly installed in the last quest) is:

```
solana config get
```

This should throw up a result similar to something like: 

