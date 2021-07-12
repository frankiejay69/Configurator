curl https://pkg.cloudflareclient.com/pubkey.gpg | sudo apt-key add -# Configurator
echo 'deb http://pkg.cloudflareclient.com/focal main' | sudo tee /etc/apt/sources.list.d/cloudflare-client.list
sudo apt update
sudo apt install 
warp-cli register
warp-cli connect
cloudflare-curl https://www.cloudflare.com/cdn-cgi/trace/warp
//dns only 
warp-cli set-mode doh
//warp doh
warp-cli set-mode warp+doh
//for additional commands
warp-cli --help
