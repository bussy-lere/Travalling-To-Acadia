import numpy as np
from matplotlib import pyplot as plt

# load in data
in_bloom = np.loadtxt(open("in-bloom.csv"), delimiter=",")
flights = np.loadtxt(open("flights.csv"), delimiter=",")

# Plot the histograms
plt.figure(1)
plt.subplot(211)

plt.hist(flights, range = (0, 365), bins = 365)
plt.title("Flights each day of the year" )
plt.xlabel("day of the year")
plt.ylabel('flight Count')

plt.subplot(212)

plt.hist(in_bloom, range = (0, 365), bins = 365)
plt.title("Flowers that begin to bloom each day of the year" )
plt.xlabel("day of the year")
plt.ylabel('flower Count')

plt.tight_layout()

plt.show()
