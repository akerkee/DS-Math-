#Three lines to make our compiler able to draw:
import sys
import matplotlib
matplotlib.use('Agg')

import pandas as pd
import matplotlib.pyplot as plt

health_data = pd.read_csv("data.csv", header=0, sep=",")

health_data.plot(x ='Кітап коды', y='Бағасы', kind='line')
plt.ylim(ymin=0)
plt.xlim(xmin=0)

plt.show()

#Two lines to make our compiler able to draw:
plt.savefig(sys.stdout.buffer)
sys.stdout.flush()


def slope(x1, y1, x2, y2):
  s = (y2+y1)*(x2+x1)
  return s
print(slope(140,20,12,98))


def my_function(x):
  return 5*x + 60

print (my_function(135))


import pandas as pd
import numpy as np
health_data = pd.read_csv("data.csv", header=0, sep=",")
x = health_data["Кітап коды"]
y = health_data["Әдеби кітаптар саны"]
slope_intercept = np.polyfit(x,y,1)
print(slope_intercept)
