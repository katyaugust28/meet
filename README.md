FEATURE 1: FILTER EVENTS BY CITY
    As a user
    I should be able to “filter events by city”
    So that I can see the list of events that take place in that city

Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.
    Given user hasn’t searched for any city
    When the user opens the app
    Then the user should see a list of all upcoming events
    
Scenario 2: User should see a list of suggestions when they search for a city.
    Given the main page is open
    When user starts typing in the city textbox
    Then the user should see a list of cities (suggestions) that match what they’ve typed

Scenario 3: User can select a city from the suggested list.
    Given the user was typing “Berlin” in the city textbox
    And the list of suggested cities is showing
    When the user selects a city (e.g., “Berlin, Germany”) from the list
    Then their city should be changed to that city (i.e., “Berlin, Germany”)
    And the user should receive a list of upcoming events in that city

FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS
    As a user,
    I should be able to show and hide an event's details
    So that I can learn more about an event or continue scrolling without too much detail

Scenario 1: An event element is collapsed by default
    Given a user wants to view a list of events
    When initially accessing the app
    Then they should be able to scroll through all the available events easily without too much detail

Scenario 2: User can expand an event to see its details
    Given a user wants to learn more about an event
    When the event is of particular interest
    Then they should be able to easily learn more with a click of a button

Scenario 3: User can collapse an event to hide its details
    Given a user wants to hide details
    When they decide they want to continue searching for other events
    Then they should be able to collapse an event to its details with the click of a button


FEATURE 3: SPECIFY NUMBER OF EVENTS
    As a user,
    I should be able to specify the number of events shown
    So that I can more efficiently search for events of interest

Scenario 1: When user hasn’t specified a number, 32 is the default number
    Given a user initially logs in
    When initially accessing the app
    Then they should initially be shown a list of events to begin browsing

Scenario 2: User can change the number of events they want to see
    Given a user wants to view a specific number of events 
    When the user selects "number of events"
    Then they should be shown the specified number of events


FEATURE 4: USE THE APP WHEN OFFLINE
    As a user,
    I should be able to use the app when offline
    So that I can check events I previously looked for before leaving the internet

Scenario 1: Show cached data when there’s no internet connection
    Given a user leaves internet connection
    When they had an event previously loaded prior to leaving the internet connection
    Then they should continue to have access to that event's details

Scenario 2: Show error when user changes the settings (city, time range)
    Given a user changes a previously loaded setting
    When they leave an internet connection
    Then the user should be shown an error page


FEATURE 5: DATA VISUALIZATION
    As a user,
    I should be able to view a chart with upcoming events in each city
    So that I have an easy visual to reference

Scenario 1: Show a chart with the number of upcoming events in each city
    Given a user wants to see a visual of the upcoming events
    When they specify a city
    Then they should be shown a chart with the number of upcoming events in that city

