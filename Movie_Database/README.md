How to run:
Step 1: Go to : https://dbfiddle.uk/
Step 2: Click on MySQL
Step 3: Copy create_tables.sql into the dbfiddle editor.
Step 4: Use the "+" button below the editor to add a new file. Paste data.sql.
Step 5: Use the "+" button below the editor to add a new file. Paste procedures.sql.
Step 6: Click Run at the top of the screen.
Step 7: Use the "+" button below the editor to add a new file. Run the following: 
SELECT * FROM Users;
SELECT * FROM Movies;
SELECT * FROM Watchlist;
SELECT user_id FROM Users WHERE username = 'alice';
SELECT movie_id FROM Movies WHERE title = 'Toy Story';
Step 8: Adding a New User:
CALL CreateUser('new_user', 'new_user@example.com');
Adding a new Movie:
CALL AddMovie('Interstellar', 'Sci-Fi', 2014, 'Christopher Nolan');
CALL AddToWatchlist(4, 5, 'To Watch');
CALL GetUserWatchlist(4);
Step 9: Show movies based on a specific genre
SELECT title, genre, release_year, director
FROM Movies
WHERE genre = 'Sci-Fi';
Step 10: See if a movie is in a user's watchlist:
CALL IsInWatchlist(4, 4, @isIn);
SELECT @isIn AS InWatchlist;
Step 11: Clear the watchlist:
CALL ClearUserWatchlist(4);
CALL GetUserWatchlist(4);


