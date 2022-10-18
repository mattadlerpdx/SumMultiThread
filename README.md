# SumMultiThread


/*
 * CS 532: sum.c: repeatedly sum numbers using multiple threads
 */

/*
 * sum: compute the value of numthreads * (sum of all integers from 0 to Round)
 * for every value of Round from 1 to numrounds
 * the program also uses a closed-form solution to check the result after each round. if it finds
 * an error, then it exits.
 *
 * build like this ---> gcc -g -Wall -Werror sum.c -o sum -lpthread
 *
 * the code as-is has no synchronization, and so it exits with an error nearly every single time.
 * your assignment is to create two "fixed" versions of this code.
 * 1. a version that calculates the correct answer but continues to inefficiently update the
 *    the "Total" global variable within the inner loop of each thread. this version should be
 *    called "sum_fix1.c"
 * 2. a more-efficient version in which each thread computes its own sum locally before updating
 *    the global "Total" after computing its local sum. this version should be called "sum_fix2.c"
 *
 * Instead of two different programs you may create a single "sum_fix.c" that satisfies
 * both (1) and (2), but then you need to
 * provide a way for the user to toggle between (1) and (2) from the command line.
 */
