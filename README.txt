Written by Ben Autrey: https://github.com/bsautrey

---Overview---

disk_list.py can be used when you would like work with python lists that are too big to fit into memory. It creates a disk-based structure that acts like python lists. It supports append() and iteration, e.g. for item in disk_list:, etc.

Each disk list may only be used one time. Temporary files are automatically deleted when they have been emptied by iteration.

---Example---

To run this example:

1) Change dir to where disk_list.py is.

2) Set WORKING_DIR in the code below and run it in a python terminal (WORKING DIR is where temporary files will be written):

from disk_list import DiskList
dl = DiskList('WORKING_DIR')
rand_str = 'Cow tipping in Elysian Fields.'
for i in xrange(1000000):
    data = (i,rand_str)
    dl.append(data)
    
number_of_items = 0
for item in dl:
    number_of_items = number_of_items + 1
	
print 'NUMBER OF ITEMS:',number_of_items