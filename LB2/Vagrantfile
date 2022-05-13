Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 32400, host: 8082
  config.vm.provision "shell", inline: <<-SHELL
  sudo su -
   sudo apt-get update && sudo apt-get -y upgrade
   wget https://downloads.plex.tv/plex-media-server/1.9.1.4272-b207937f1/plexmediaserver_1.9.1.4272-b207937f1_amd64.deb
   sudo dpkg -i plexmediaserver*.deb
   service plexmediaserver restart
   mkdir /plex-images
   mkdir /plex-shows
   mkdir /plex-videos
   mkdir /plex-music
  SHELL
end