# Spark - Simple Join
We will repeat the Join 1 exercise using spark. Instead of having 1 mapper, we will have 2 - 1 for fileA and 1 for fileB.
   - split_fileA.py as the (key, value)
   - split_fileB.py as the (key, value)

We run the mappers on the files like so:

fileA_output = fileA.map(split_fileA)  
fileB_data = fileB.map(split_fileB)

Then, we run join on the two outputs:

fileB_joined_fileA = fileB_output.join(fileA_output)

to produce fileB_joined_fileA.
