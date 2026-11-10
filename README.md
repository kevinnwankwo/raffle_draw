Unique-Winner Raffle Draw System

A CLI-based Python script built for Okoro & Sons Limited to handle a digital customer promo raffle draw. The system allows customers to submit multiple tickets to boost their odds while guaranteeing that no individual customer can win more than once.

Key System Features

Dynamic Ticket Accumulation: Customers can submit multiple tickets under their unique Customer ID. Each ticket acts as an entry in the pool, statistically scaling up their chances of winning.
Case-Insensitive Input Validation: Normalizes entries to uppercase and trims whitespaces so that inputs like `"cust-01 "` and `"CUST-01"` map to the exact same customer database profile.
Empty Entry Guard: Rejects blank input fields to prevent invalid or anonymous tickets from polluting the draw pool.
Unique Winner Enforcement: Restricts raffle results to 5 distinct customers using an anti-duplication filter during selection.
Minimum Participation Check: Assures that at least 5 unique customers have submitted tickets before running the draw, preventing runtime crashes.
Raffle Logic & Execution Rules

Submission Phase: The program continuously collects Customer IDs until the entry clerk inputs `DONE`.
Pool Count Tracking: Displays real-time updates of total entries currently in the electronic ticket drum after each addition.
Selection Phase: Picks tickets at random from the collective pool. If the owner of the selected ticket has already won, the script drops the ticket and picks another until 5 unique slots are filled.

Technical Requirements

Python Version: Python 3.x

Dependencies: Uses the standard built-in `random` module. No external installations needed.

Setup & Execution Guide

Save the code locally as `raffle.py`.
Launch your command line environment.

Execute the script with the following command:

```bash
   python raffle.py
   ```
