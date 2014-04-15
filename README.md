# QuizApp

Week 8 project for Makers Academy designed to introduce us to Rails, mostly developed with @mfolsom. This app lets you complete simple true/false questions, add your own questions and see your stats. It was made with Rails (and various bits of associated magic), styled with Sass and tested with Cucumber and Rspec. You can play with it [here](http://infinite-earth-4893.herokuapp.com/).

## How it works

The first thing you have to do before you use the app is sign up (or sign in) so that we can track your answers. Then, you'll be presented with a true or false question to answer (by pressing either the giant "True" button, or the giant "false" button). Once you've done that, you'll be told whether or not your answer was correct, and then you'll be given a new question to answer. This continues until you've answered all the questions (which won't take long, as we only seed three...). If you think there should be more questions, you can help us by adding one yourself. You can't answer your own questions, but it helps the site. At any time (though we'd suggest answering a few questions first), you can check out your statistics. Your profile page lists your name and current score. The stats page tells you more general statistics about the site: the hardest and easiest questions; the number of questions; and the best players. Simple.

### Users

User sign up with an email address, a username and a password. They can have many Questions and Answers. They can ask new Questions. They know their score (calculated as the percentages of all their answers which are correct).

### Questions

Questions know their maker. They have many answers. They know if a given user has answered them before. They also know how difficult they are (using the same calculation the User does to work out their score).

In addition, the class Question can serve up a random question for a given User by first ordering the questions randomly, then filtering out those questions which that User has asked or answered already.

### Answers

Which means that answers need to know if they're correct or not, and which users and questions they belong to. So they do.