## Concerts Domain Project
This project models a Concert domain with three main entities: Bands, Venues, and Concerts. The project uses raw SQL queries for database interactions, avoiding any ORM frameworks like SQLAlchemy. The project also includes Python methods to perform operations on these entities and their relationships.

## Project Structure
db_setup.py: Sets up the SQLite database and creates tables (bands, venues, concerts).
seed_data.py: Seeds the database with initial test data (bands, venues, and concerts).
band.py: Defines the Band class and its methods for interacting with the database.
venue.py: Defines the Venue class and its methods.
concert.py: Defines the Concert class and its methods.
main.py: Test file to verify the functionality of the methods and models.
migrations/: Contains SQL migration files to create tables.
## Setup Instructions
Clone the repository:

bash
Copy code
git clone <your-repo-url>
cd concerts-domain
Create the database and tables:

Run the following command to execute the migrations and create the SQLite database (concerts.db):

bash
Copy code
python db_setup.py
Seed the database:

## To insert initial data into the database, run:

bash
Copy code
python seed_data.py
This will add:

Band: "The Rolling Stones" (from London)
Venue: "Wembley Stadium" (located in London)
Concert: A concert by "The Rolling Stones" at "Wembley Stadium" on "2023-08-01".
Run the Tests:

## You can run the tests for the methods and models by executing:

bash
Copy code
python main.py
This will print out the results for the various object relationships (e.g., bands, venues, concerts).


## methods and Functionality
Band
Band.concerts(): Returns a list of all concerts the band has played.
Band.venues(): Returns a list of all venues the band has performed at.
Band.play_in_venue(venue, date): Creates a new concert for the band at the given venue on the specified date.
Band.all_introductions(): Returns a list of all introductions for the band at different concerts.
Band.most_performances(): Returns the band that has played the most concerts.
Venue
Venue.concerts(): Returns a list of all concerts held at the venue.
Venue.bands(): Returns a list of all bands who have performed at the venue.
Venue.concert_on(date): Finds and returns the first concert on a given date.
Venue.most_frequent_band(): Returns the band that has performed the most times at the venue.
Concert
Concert.band(): Returns the band that played at the concert.
Concert.venue(): Returns the venue where the concert was held.
Concert.hometown_show(): Returns True if the concert was in the band's hometown, otherwise False.
Concert.introduction(): Returns a string with the band's introduction for the concert (e.g., "Hello London!!!!! We are The Rolling Stones and we're from London").
## Requirements
Python 3.x
SQLite3 (comes pre-installed with Python)
## How to Contribute
Feel free to fork this repository and submit pull requests. Please ensure that all changes are tested thoroughly before submitting.
## author 
mercy mumbua
