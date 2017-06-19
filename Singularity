bootstrap: docker
from: ubuntu:latest


%post
	
	apt-get update
	apt-get install -y build-essential
	apt-get update
	apt-get -y install locales
	apt-get -y install cmake
    apt-get -y install g++
    apt-get install -y python3-dev python3-pip \
    libxft-dev libfreetype6 libfreetype6-dev python3-tk
    apt-get clean
    locale-gen en_US.UTF-8

    pip3 install matplotlib
    pip3 install Pillow 
    
%environment
	echo "Restoring environment"
	export LC_ALL=C
    export PATH=/bin:/sbin:/usr/bin:/usr/sbin:$PATH


%test
	python3 -c "import matplotlib"
