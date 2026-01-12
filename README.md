# -to-compute-the-number-of-characters-words-and-lines-in-a-file.
# Use 'with' to automatically close the file after reading
with open('D:/a.txt', 'r') as k:
    char, wc, lc = 0, 0, 0  # Initialize counters for characters, words, and lines
    
    for line in k:
        lc += 1  # Increment line count for each line in the file
        
        # Count characters: includes spaces, newlines, etc.
        char += len(line)
        
        # Split the line into words and count them
        words = line.split()  # This automatically handles multiple spaces
        wc += len(words)
        
    # Output the results
    print("The number of chars is %d" % char)
    print("The number of words is %d" % wc)
    print("The number of lines is %d" % lc)
