Open the terminal and paste this

wget http://repo.continuum.io/miniconda/Miniconda3-latest-Linux-armv7l.sh
sudo md5sum Miniconda3-latest-Linux-armv7l.sh
sudo /bin/bash Miniconda3-latest-Linux-armv7l.sh

On the agreement hit enter about 44 times to get to the prompt for yes if you press it too 1 to many times
it defaults to no and to have to repeat the 
sudo /bin/bash Miniconda3-latest-Linux-armv7l.sh

again to restart the prompt for the licence agreement to say yes to.

Once that has been done to test first close the terminal and open a new one. In the new one type 

conda

If you get a list of commands this step worked.

Then go to https://github.com/jjhelmus/berryconda and download

Berryconda3-2.0.0-Linux-armv7l.sh

It will be in the downloads folder of the pi. Cut it and put it in the main folder next to the miniconda
download. Once it is there paste

chmod +x Berryconda3-2.0.0-Linux-armv7l.sh 
./Berryconda3-2.0.0-Linux-armv7l.sh

in the terminal. It will prompt you with a similar agreement but this one has no default 
and needs a yes or no. Once this is done close the terminal and open a new one and type 

python --version

A version of 3.6 or higher should be installed.
now install the libraries needed for data visualization. 

data visualiation libraries:

numpy
scipy
matplotlib
statsmodels
pandas
seaborn

ex. conda install numpy

Once those are installed open up Thonny Python IDE and run the following code:


import matplotlib
import matplotlib.pyplot as plt
import numpy as np

# Data for plotting
t = np.arange(0.0, 2.0, 0.01)
s = 1 + np.sin(2 * np.pi * t)

fig, ax = plt.subplots()
ax.plot(t, s)

ax.set(xlabel='time (s)', ylabel='voltage (mV)',
       title='About as simple as it gets, folks')
ax.grid()

fig.savefig("test.png")
plt.show()


A line graph should pop up in a window. If so congrats you are done!
