# Ruby Console & Object Oriented Ruby

## The Plan

This pairing lab does not have a designated place to switch drivers. Instead, every 30 minutes the pair's responsibilities should swap. The driver becomes the navigator, and vice versa.

To minimize extra cloning and forking, this project should be completed in only one person's Github account, on one computer.

## What is a `console`

A programming console is a coding environment to run text based code. `console`s give developers a way to interact with their domain. Similar to adding a breakpoint in your code ( `binding.pry` ), `console`s have access to all the Ruby classes and objects you have created in your program.

This lesson contains a console that you can use. To enter the console session, run `ruby tools/console.rb`. You'll be able to test out the methods that you write here.

## Domain mapping

Before you start building the domain outlined below, read over the application interface ("Deliverables") and discuss what the relationship of these objects are. What belongs to what? What has many of another? What links objects together? What object serves as a source of truth for connecting two other objects?

## Instructions

*After discussing your domain*, your goal is to build out all of the methods listed in "Deliverables". Do your best to follow Ruby best practices. For example, use higher-level array methods such as `map`, `select`, and `find` when appropriate in place of `each`.

  --  Make sure you are testing your code as you go! --

Look at the contents of the `console.rb` file and use the commented out code to guide writing your API. Comment out a line or section at a time and verify that 1. your code executes without error and 2. your code returns the expected data.

## Deliverables

Implement all of the methods described below

### `Course`

* Course.all
  * returns **all** of the course instances
* Course.find_by_subject(subject)
  * given a string of the subject, returns the **first course** whose subject matches
* Course.all_subjects
  * returns a collection of all the subjects of all courses, without duplications
* Course#enrollments
  * returns a collection of enrollment objects for the given course
* Course#class_list
  * returns a collection of the full names of each student enrolled in the given course

### `Enrollment`

* Enrollment.all
  * returns all enrollment instances
* Enrollment#course
  * returns the **course object** for that given enrollment
* Enrollment#student
  * returns the **student object** for that given enrollment
* Enrollment#semester
  * returns a string of the given semester for the enrollment, e.x. `"Fall 2024"`

### `Student`

* Student.all
  * returns **all** of the student instances
* Student#full_name
  * returns a string of the students full name
* Student#enroll(course, semester)
  * given a **course object** and a semester (as a string), creates a new enrollment and associates it with that course and student. An `Enrollment` belongs to a `Student` and a `Course`. The method should return the new `Enrollment` object.
* Student#buy_supply(kind)
  * given a string of the kind of supply, creates a new school_supply and associates it with that student. A `SchoolSupply` belongs to a `Student`. The method should return the new `SchoolSupply` object.
* Student#school_supplies
  * returns a collection of all of the given student's SchoolSupplies

### `SchoolSupply`

* SchoolSupply.all
  * returns **all** the school_supply instances
* SchoolSupply#student
  * returns the **student object** for that given school_supply
* SchoolSupply.find_all_by_kind(kind)
  * returns a collection of school_supply objects with the given kind

## Questions:

Once you've completed this project, discuss the questions below.

- What other objects might fit in this domain?

- What may be the benefit of changing `semester` into its own class? What attributes would it have? What object would it belong to?

- What other methods could be added and useful in this domain?

