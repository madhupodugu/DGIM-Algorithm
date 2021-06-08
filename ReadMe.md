<h2>Mining Data Streams through DGIM Algorithm</h2>

This project implements DGIM algorithm using Python. Please download the zipped folder 
and run the dgim_alg.py file using Python IDE or through Pycharm IDE. 

DGIM algorithm counts no of 1's in a particular window using Buckets. Each bucket,
stored in the window, contains the size(no of 1's from beggining to end) and a timestamp
of the rightmost 1 bit. The no of 1's in each bucket must be a power of 2, the right end of a 
bucket should be a 1, there should be no overlap between one bucket to another, and there can be 
only one or two buckets of any given size, up to the maximum size. 

The dgim_alg.py first takes the input paragraph and converts all letters to their ASCII representation 
and then their binary form. Once the paragraph has converted to 0/1 stream, the algorithm creates buckets 
for the first 32 bits in the stream, and when new bit enters, it slides the window (N=32) so that the 
window contains only 32 bits. For every new bit 1, it creates the bucket with size 1 and merges the other buckets
if any of the buckets sizes appear 3 times. Lastly, after the merge, it estimates the no of 1's by adding all the 
buckets size and adds the only the half the size of a bucket that overlaps with the window (N=32). 
