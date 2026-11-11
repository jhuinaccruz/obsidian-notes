# Day 1
## Tuples

__Tuple__: Unlike a list, represents different facts about a single observed item
>*Tuples look like lists, but we use parenthesis, not square brackets, to define them*

>[!warning]
>*Tuples are immutable, unlike lists.*

## Iterating over Tuples
```run-python
my_movies = [("No", 4), ("Rogue One", 4.5), ("Casablanca", 5)]

best_rating = 0 # Initialize with a value that is definitely beat
best_movie = "none"
for movie, rating in my_movies:
    if rating > best_rating:
        best_rating = rating
        best_movie = movie

print("Best movie: " + best_movie + "...rating = " + str(best_rating))
```

## Example
>[!example]
>*The list below contains tuples of (Star Wars movie name, Rotten Tomatoes score). Produce a list (using .append() and a foreach loop) that contains only the titles of movies that scored 80 or above. If you're not sure how to proceed, try to solve it with your neighbor.*

```run-python
sw_movies = [('The Phantom Menace', 52),
('Attack of the Clones', 65),
('Revenge of the Sith', 80),
('Rogue One', 84),
('Solo', 70),
('Star Wars', 92),
('The Empire Strikes Back',94),
('Return of the Jedi', 82),
('The Force Awakens', 93),
('The Last Jedi', 90),
('The Rise of Skywalker', 51)]

output = []

for (name, score) in sw_movies:
    if score > 79:
        output.append(name)


print(output)
```

# Day 2
>[!abstract]
>- List-of-lists
>- Nested Loops
>- List Comprehensions

__Lists-of-Lists__: a data structure that lends itself to nested loops
__