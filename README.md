# NAME OF REPOSITORY: Checkpoint_Sorting_and_searching_algorithms



# DESCRIPTION: A repository for Checkpoint Sorting and searching algorithms. This repo houses an algorithm which is described below.



# An insertion_sort algorithm using the following instructions:

# INSTRUCTIONS
# 1.  Each time work only with the first i-1 element from of the array
# 2.  Pick element arr[i] and insert it into sorted sequence in the array from 0 to i-1.


# Below is a discription of what the alorithm is doing(algorithm steps to solve the problem):

# Naming the algorithm.

            ALGORITHM myinsertion_sort

  
# Declaration of variables to be used as counters and limiting sort size to 100 numbers.

             i, j, n, arr_key : INTEGER;
             set_array : ARRAY_OF INTEGER[100];

# Get input from user using repeat_until loop.

             REPEAT
             Write ("Number of items to be sorted (between 1 and 100): ");
             Read (n);
             UNTIL (n > 0 AND n <= 100)

# Take user inputs to create an array to be used.

             Write ("Enter numbers sequentially:");
             FOR i FROM 0 TO n-1 STEP 1  DO
             Read (set_array[i]);
             END_FOR

# Assign item to array_key

             FOR i FROM 1 TO n-1 STEP 1  DO
             arr_key = set_array[i];

# Set index for previous item

             j = i - 1;

# Loop while the index is more than 0 and the current array_key is greater than the previous jth element

             WHILE (j > 0 and set_array[j] > arr_key) DO

# Increase the position j of the previous element by 1

             set_array[j + 1] = set_array[j];

# Create a position at j - 1 as j

             j = j - 1;

# Move the element into the j location

             set_array[j + 1] = arr_key;

# End while loop and for statements                     
             END_WHILE            
             END_FOR

# Display new array

             Write (set_array);                                     

# End insertion_sort algorithm
 
