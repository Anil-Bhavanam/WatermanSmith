# WatermanSmith

The provided code is an implementation of the local alignment algorithm using dynamic programming. Local alignment is a method used to identify the best-matching subsequences between two sequences, which can be DNA, RNA, or protein sequences. This algorithm finds the optimal alignment by maximizing a scoring function that considers substitutions, gaps, and matches.

The code defines a class named Solution that contains a method called local_alignment. The method takes four parameters: sequence_A (the first sequence), sequence_B (the second sequence), substitution (a dictionary representing the substitution matrix), and gap (the gap penalty).

The code begins by importing the necessary libraries, pandas and numpy, to work with data frames and arrays. It then creates a pandas DataFrame called df using the substitution dictionary and prints the substitution matrix.

Next, the code converts the substitution matrix from a DataFrame to a numpy array called substitution_matrix. It also determines the lengths of sequence_A and sequence_B.

The code initializes two matrices, est_matrix and pointerTable, both filled with zeros. These matrices will store the scores and pointers for the alignment.

A nested loop is used to fill the est_matrix based on the dynamic programming algorithm. The code calculates the scores for each cell in the matrix by considering three possibilities: a match (diagonal), a gap in the first sequence (top), or a gap in the second sequence (left). The maximum score among these possibilities is assigned to the current cell. The pointerTable is also updated based on which possibility was chosen.

After filling the est_matrix and pointerTable, the code finds the highest score and its corresponding indices in the matrix. It starts from this position and traces back the alignment path by following the pointers in pointerTable. The aligned subsequences are constructed by appending the characters to rx and ry lists.

Finally, the aligned subsequences are reversed, joined into strings, and printed to display the local alignment result.

Note: The code snippet you provided is incomplete and lacks the necessary indentation at the end. The final lines of the code, where rx and ry are reversed and printed, should be indented to be included within the local_alignment method.
