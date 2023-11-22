function generateWalletAddress() {
    const privateKey = bitcoin.ECPair.makeRandom().toWIF();
    const publicKey = bitcoin.ECPair.fromWIF(privateKey).getAddress();
    return publicKey;
}

const walletAddress = generateWalletAddress();
document.getElementById('wallet-address').innerText = walletAddress;
