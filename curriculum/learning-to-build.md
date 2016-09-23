# Learning to build

## Prerequisites

Understanding of at least one language. Knowledge of git is nice, but not essential.

## Plan

The plan will be split into four phases. Each phase will have you build the same application in a different environment. You'll build a commandline tool, a ncurses based GUI, a application in your preferred GUI toolkit, and a webapp.

You will build a ticket booking app. It will have tickets for events/movies/shows, etc. The app will allow the user to search with his preferences and book a ticket.

#### Phase 1 - Commandline App:
- The commandline app will allow a user to interactively book a ticket based on his search parameters (date, name, genre, type)
- All data will be read from a rdbms database
- When a ticket is available for the event the user wants he will have to answer certain questions to finish the booking
- Payment will be handled via credits in the user's account

###### Details:
- It will accept endless commands, i.e. I start the app, and see a menu. Through the menu I can either select "showing soon", "showing soon by genre", "showing soon by type", search.
- When I select the first three options, I see table formatted output, and I can type next to go to the next page, or book using an event number/id
- So on the listing page two I can say "book 3", or "book <event id>"
- It then takes me into a booking view, where it asks me questions like number of seats, name of one person attending
and then shows me a booking confirmation view that I have to confirm/reject.
- A view where I can see my credits (everyone starts with a random number between 500 - 5000), each event between a number 150-300
like movies are 250, plays 300, music even 150
- In the search view I'm shown a help message describing keywords. For example "cost:200 genre:comedy type:movie" will show me all comedy movies that cost less than 200.

#### Phase 2 - ncurses app:
- All the above features
- Uses the ncurses library to create a basic gui
- User can add credits to his account using coupons
- Coupons will follow a certain pattern in helping determine what its values are

#### Phase 3 - Native-ish GUI app:
- All the above features
- User login using email
- User can add credits to his account using a payment gateway
- User can transfer credits to another user (using email)

#### Phase 4 - Web App:
- All the above features
- Admin login
- Admin can CRUD events
- Admin can add credits to user
