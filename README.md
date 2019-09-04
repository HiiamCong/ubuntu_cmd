# ubuntu_cmd
This repo contains commands for fixing error on ubuntu and some nice tricks to treat this ***king os

# view GPU info
nvidia-smi

# install GPU realtime info
nvtop
https://github.com/Syllo/nvtop

# copy multiple file from a folder to another folder
cp -a /source/. /dest/

# view disk space
df -h
du -h | sort -h

# view processes running with python
ps -ef|grep python

# change right all file in a folder
sudo chmod -R 777 folder

# convert sample rate audio with ffmpeg
ffmpeg -i file1.mpg -ar 16000 file1-enc.mpg

# limit W of GPU using (use for auto reboot problem when training with GPU)
sudo nvidia-smi -pl 150

# check tensorflow-gpu
import tensorflow as tf
sess = tf.Session(config=tf.ConfigProto(log_device_placement=True))

# turn off auto on base env anaconda
conda config --set auto_activate_base false

# fix error can not install package or clone git
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null

# remote jupyter notebook from server
1. on server: 
    jupyter notebook --no-browser --port=8889
2. on local:
    ssh -N -f -L localhost:8888:localhost:8889 -p55022 vbee@14.160.70.42
    localhost:8888

# install .deb file
sudo dpkg -i /path/to/deb/file
sudo apt-get install -f
