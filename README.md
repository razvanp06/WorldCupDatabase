Overview
The project focuses on processing a dataset of World Cup matches and importing it into a PostgreSQL database. It includes an automation script for data insertion and a suite of analytical queries to extract tournament statistics.

Key Features
Relational Schema: A normalized database structure with primary and foreign key constraints.

Automated Data Pipeline: A Bash script (insert_data.sh) that reads raw CSV data and populates the database while maintaining data integrity.

Data Analysis: A dedicated SQL script (queries.sh) providing insights such as tournament winners, average goals, and team statistics.

Tech Stack
Database: PostgreSQL

Scripting: Bash (Shell Scripting)

Environment: Linux/Terminal

Database Schema
The database architecture consists of two main tables:

teams: Stores unique names and IDs of all participating nations.

games: Stores match details, including year, round, goals, and references to the teams table via winner and opponent IDs.

How to Run
Clone the repository:
git clone https://github.com/your-username/world-cup-database.git

Setup the Database:
Create the database in PostgreSQL:
CREATE DATABASE worldcup;

Import the schema:
psql -U postgres -d worldcup < worldcup.sql

Populate Data:
Run the Bash script to import data from games.csv:
chmod +x insert_data.sh
./insert_data.sh

Run Analytics:
Execute the query script to see the results:
./queries.sh
