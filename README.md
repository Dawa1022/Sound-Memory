# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Dawa Sherpa**

Time spent for required functionality: **1 hours and 30 minutes** spent in total
Time spent for additional feautureL **3 hours** spent in total

Link to project: (https://glitch.com/edit/#!/sound-memory?path=index.html%3A1%3A0)

## Required Functionality

The following **required** functionality is complete:

- [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [x] "Start" button toggles between "Start" and "Stop" when clicked.
- [x] Game buttons each light up and play a sound when clicked.
- [x] Computer plays back sequence of clues including sound and visual cue for each button
- [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [x] User wins the game after guessing a complete pattern
- [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [x] Buttons use a pitch (frequency) other than the ones in the tutorial
- [x] More than 4 functional game buttons
- [x] Playback speeds up on each turn
- [x] Computer picks a different pattern each time the game is played
- [x] Player only loses after 3 mistakes (instead of on the first mistake)

## Video Walkthrough

Here's a walkthrough of implemented user stories:
<ul>
   <li> This GIF shows that the player wins game after succesfully guessing all the patterns</li>
      <img src="img/game_complete.gif">
   <li> This GIF shows that the player loses after 3 mistakes</li>
      <img src="img/game_lost.gif">
   <li> This GIF shows that the computer picks a different pattern each time the game is played</li>
      <img src="img/random_pattern.gif">
   </ul>

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.

 - The following resources were used for the completion of this project:
   <ul>
   <li>https://www.w3schools.com/</li>
   <li>https://colours.neilorangepeel.com/</li>
   <li>https://coolors.co/</li>
   </ul>

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)
 
 - In the script.js file, in order to create random secret pattern each time the game was started, I had created the random number generator function “getRandom()” and called it in the “startGame()” function. This way each time the “Start” button was pressed 8 random numbers would be generated and those 8 random numbers would be added to the “pattern” array. But the game did not work as I had expected, when I pressed the “Start” button, each time it would generate 8 new random numbers but when I pressed the “Stop” button and pressed the “Start” button again it would generate 8 other new random numbers and add it to the same “pattern” array, so the "pattern" array length would be 16, then 24 and kept adding 8 new numbers if I kept stopping and starting the game without refreshing the page. I found this bug by opening the console feature which allowed me to see the “pattern” array log. I overcame this challenge by figuring out that whenever I pressed the "Stop" button I wanted the program to empty the “pattern” array and not add new numbers to the same array, so I added an if statement in the "stopGame" function that would make the “pattern” array an empty array, if the “pattern” array length was more than 0. By doing this, the “pattern” array length would be 8 each time the game was started, and it would be empty each time the game was stopped, so the game would always have a 8 new random numbers as the pattern.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)
   [YOUR ANSWER HERE]

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)
   [YOUR ANSWER HERE]

## License

    Copyright [Dawa Sherpa]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
