# cv-ai4all-pton
Computer Vision Project for AI4All at Princeton, 2017.

# Installation

```BASH
#IF VIRTUALENV NEEDED: make a virtualenv (https://packaging.python.org/guides/installing-using-pip-and-virtualenv/)
alias python=python3; PYTHONPATH=""
python3 -m pip install --user virtualenv

#IF VIRTUALENV NEEDED:  create the environment in folder "p3env"; change p3env to any path you'd like
VPATH=p3env
python3 -m virtualenv $VPATH
echo 'alias python=python3; PYTHONPATH=""' >> $VPATH/bin/activate
source $VPATH/bin/activate

# clone repo into BASEDIR-- set it to be the base directory of the folder
BASEDIR=
cd $BASEDIR
git clone https://github.com/lujonathanh/cv-ai4all-pton.git
cd cv-ai4all-pton

# install requirements
while read f; do brew install $f; done < requirements.txt

# install python requirements
pip install -r requirements.txt

#IF VIRTUALENV NEEDED: install the kernel so that jupyter can find the ipykernel
sudo python -m ipykernel install --user

#IF VIRTUALENV NEEDED: if in virtual environment, deactivate the package
deactivate
```


# TODO
* Test script that confirms installation was successful