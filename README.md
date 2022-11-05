# hightechfarm-qt-linux
Coin properties;
Compiling OS  Ubuntu 18.04 LTS;
Source branch  2.13;
Algorithm  Scrypt Proof of Work and Proof of Stake;
Coin name  --  hightechfarm;
Coin abbreviation  --  HFARM;
Public address letter  --  H;
RPC port   ---   9137;
P2P port   ---  9138;
Block reward  --  50 coins;
Block reward (PoS)  --  5 coins;
Website URL  http://hightechfarm.eu;
Github URL   https://github.com/hightechfarm;
Last PoW block  ---  block 100000;
Min. stake age  --  1 hours;
Max. stake age  -- Unlimited;
Coinbase maturity   5 ( + 1 default confirmation) blocks;
Target spacing 5 minutes;
Target timespan 10 minutes;
Transaction confirmations  6 ( + 1 default confirmation) blocks;
Node 1  =  node2.walletbuilders.com;
Node 2  =  harti-vrancea.go.ro;




Tutorial - Install node on Ubuntu Server 18.04

Install a node for your coin on Ubuntu Server 18.04 with the following tutorial.

Update your Ubuntu server with the following command:

sudo apt-get update && sudo apt-get upgrade -y

Install the required dependencies with the following command:

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common cmake -y

Install the repository ppa:bitcoin/bitcoin with the following command:

sudo add-apt-repository ppa:bitcoin/bitcoin

Confirm the installation of the repository by pressing on the enter key. enter

Install Berkeley DB with the following command:

sudo apt-get update && sudo apt-get install libdb4.8-dev libdb4.8++-dev -y

Download the Linux daemon for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=fb71734dca715a118bd0f2ae1bb9d01d8740d965275c1d1efc&filename=hightechfarm-daemon-linux.tar.gz" -O hightechfarm-daemon-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf hightechfarm-daemon-linux.tar.gz

Download the Linux tools for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=fb71734dca715a118bd0f2ae1bb9d01d8740d965275c1d1efc&filename=hightechfarm-qt-linux.tar.gz" -O hightechfarm-qt-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf hightechfarm-qt-linux.tar.gz

Type the following command to install the daemon and tools for your wallet:

sudo mv hightechfarmd hightechfarm-cli hightechfarm-tx /usr/bin/

Create the data directory for your coin with the following command:

mkdir $HOME/.hightechfarm

Open nano.

nano $HOME/.hightechfarm/hightechfarm.conf -t

Paste the following into nano.

rpcuser=rpc_hightechfarm
rpcpassword=dR2oBQ3K1zYMZQtJFZeAerhWxaJ5Lqeq9J2
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1

Save the file with the keyboard shortcut ctrl + x.

Type the following command to start your node:

hightechfarmd
