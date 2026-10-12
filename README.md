# 💸 SpendWise

**A personal finance app for Android that turns budgeting from a solo chore into something you can do with friends.**

SpendWise is the semester project I built with four teammates in Georgia Tech's CS 2340 (Objects and Design) in fall 2025, and we took it from a login screen and some placeholder pages to a working app with budgets, an expense log, group savings, charts, notifications, and an AI chatbot. This repo is a write-up of the product and my part in it.

## What it does

- **Expense log.** Users record spending by category and date, and every other feature in the app reads from it.
- **Budgets.** Users set a budget for each of 5 spending categories on a custom plan page, and the app tracks how full each one is as expenses come in.
- **Savings circles.** Friends can invite each other into a circle with a shared goal, and each member's individual target is worked out from the circle's goal.
- **Dashboard charts.** Pie and bar charts break down spending by category so users can see where their money went at a glance.
- **Notifications.** The app warns users when a budget is filling up or a deadline is close, and each alert links straight to the expense log.
- **AI chatbot.** A chat assistant built on Gemini 2.5 Flash answers questions inside the app, and once a conversation passes 3 messages it summarizes the older ones, so long chats do not lose context.

## My part

I owned the expense log screen, the budgets page, and the calendar date selection that both of them run on, and later in the semester I took on the profile page, which shows relevant user statistics and lets users pick a profile picture from a set of presets. I also wrote a lot of the unit tests for my screens and cleaned up redundant code along the way. Across the semester I opened 15 pull requests. Because the budgets page depended on the expense log and the savings circles depended on both, I spent a lot of time making sure my pieces matched what my teammates needed from them before they started building on top.

## How we built it

| Layer | What we used |
|---|---|
| App | Java, Android Studio, MVVM architecture |
| Accounts and data | Firebase |
| AI | Gemini 2.5 Flash, wrapped with the decorator pattern |
| Process | Jira sprints, GitHub pull requests, Checkstyle, unit tests |

We planned each sprint in Jira and assigned every feature to one owner, and when a teammate got busy during the first sprint, another teammate took over the nav bar and we reassigned the ticket so the board still matched reality. Every change went through a pull request. The repo passed 160 of them by the end of the semester, and the last few weeks were spent refactoring for SOLID and GRASP principles and clearing out code smells that had built up while we were moving fast.

## What I learned

Building a feature was rarely the hard part, because the hard part was the space between features, where one person's data model had to line up with what three other screens expected from it. In our first retrospective we decided to set our own deadlines a few days ahead of the real ones and hold short check-ins in the middle of each sprint, so that integration problems would come up early instead of piling up at the end; I learned that a team ships at the speed of its handoffs rather than the speed of its fastest coder.

## A note on the code

Because SpendWise was graded course work, the source stays in our team's private repository, and this repo documents the product and my contributions instead. I am happy to walk through the code or the design in a conversation.

Built with John DeVoe, Marina Chen, Oliver Cederbaum, and Harsh Singh.
