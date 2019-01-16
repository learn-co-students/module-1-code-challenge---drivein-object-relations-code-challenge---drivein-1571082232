# Object Relations Assessment

## Your Task

For this challenge, you have been given the job of creating a command line interface for your local drive-in movie theater, Happy's Sunset Drive-In! You have been asked to create a tracking tool that allows employees to know how many cars are at each movie screen.  The drive-in has many screens, and each screen can have many cars.  For the safety of all viewers, there is a limit to the number of cars that can be at a movie screen.  

## Notes

Your goal is to build out all of the methods listed in the deliverables and connect the required classes to a command line interface.

Do your best to follow Ruby best practices. For example, use higher-level array methods such as `map`, `select`, and `find` when appropriate in place of `each`

We've provided you with a tools/console.rb file, so you will be able to test out the methods that you write here.

  - **NOTE ABOUT TESTING:** You must run `tools/console.rb`––`$ ruby tools/console.rb`––from this assignment's **root directory**, not from inside the tools directory. You'll be able to test out the methods that you write here. Take a look at that file to see how you can pre-define variables and create object instances, rather than manually creating test data each time you enter a `pry` session.


**To Submit** - once you've completed all the deliverables, please copy/paste your three class definitions into the `solution.rb` file. Please don't submit the lab until we give you the signal.

## Deliverables

Implement all of the methods described below

### DriveIn

+ DriveIn#screens
  + returns all movie screens
+ DriveIn#cars_with
  + this method takes in an integer that represents the number of people in a car. This method should return all cars that have that amount of people
+ DriveIn#full_house?
  + returns true if all movie screens are at capacity
+ DriveIn#whats_playing
  + returns the names of all movies currently playing
+ DriveIn#available_movies
  + returns a hash with a top level key for every available movie, each key will point
  to a hash with a key of 'available_spots', which points to the amount of spots available
  at that screening as well as a key of 'people_watching' that points to the total number of people watching the movie.

  Ex:
  ```
  {
    it:{
      available_spots: 10,
      people_watching: 30
    },
    spider-man 2:{
      available_spots: 0,
      people_watching: 150
    }  
  }
  ```



### MovieScreen

+ MovieScreen#cars
  + Returns an array of all cars currently at _this_ movie screen
+ MovieScreen#at_capacity?
  + Returns a boolean.  The return will be true if the number of cars at _this_ movie screen is at capacity
+ MovieScreen#add_car
  + Adds an instance of a car to _this_ movie screen if the movie screen is not at capacity, creates a new car instance and returns the string "Enjoy!".  If the movie screen is at capacity, return a string that says 'Movie is sold out'
+ MovieScreen.all_screens
  + Returns all movie screens
+ MovieScreen#how_many_viewers?
  + returns a head count of how many people are watching the movie

### Car

+ Car.all
  + Returns all cars
+ Car#movie_screen
  + Returns the movie screen _this_ car is at
+ Car#passenger_count
  + Returns the number of people within _this_ car
