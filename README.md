5-Card Poker Hand Evaluator

This repository contains a C assignment that implements and tests several functions for evaluating 5‑card poker hands drawn from a standard 52‑card deck. The project includes functionality to:

    Swap cards and shuffle a deck
    Evaluate poker hands, including detecting:
        A single pair
        A flush
        A straight (with special handling for Ace-low and Ace-high straights)
        A royal flush (optional bonus function)

Repository Contents

    poker.c
    Contains the implementation of all poker hand evaluation functions along with simulation code to test these functions over millions of hands.

    README.md
    This file.

Deck and Hand Representation

    Cards: Represented as integers 0 through 51.
    Suits: Determined using card % SUITS (where SUITS is defined as 4).
    Faces: Determined using card % FACES (with FACES defined as 13).
    Face Names:

const char *face[FACES] = {"Ace", "Deuce", "Three", "Four",
                           "Five", "Six", "Seven", "Eight",
                           "Nine", "Ten", "Jack", "Queen", "King"};
How to Compile and Run

    Compile the Code
    Use GCC (or your preferred C compiler) to compile the program. For example:

gcc -O2 -o poker poker.c

The -O2 flag optimizes the code.

Run the Executable

    ./poker

    The program simulates 10 million 5‑card hands and prints the observed probabilities for the different hand types (e.g., the number of royal flushes).

Expected Results

    Royal Flush:
    There are exactly 4 royal flushes in a 52‑card deck. The theoretical probability is:
    42,598,960≈0.00000154(or about 15 royal flushes per 10 million hands)
    2,598,9604​≈0.00000154(or about 15 royal flushes per 10 million hands)

    Other Hand Evaluations:
    The simulation will also report probabilities for other hand types (pair, flush, straight, etc.), which you can compare to the theoretical values.

Simulation and Testing

The simulation code in poker.c deals random hands (ensuring no duplicate cards) and then uses your evaluation functions to count occurrences of each hand type. Testing over 10 million hands provides an empirical approximation of the probabilities, which helps confirm that your functions work as expected.
License

This project is open source and available under the MIT License.
