# Cake Day Laravel API

This repository contains the backend API for a Cake Day application, built with Laravel. The goal is to help teams keep track of developer birthdays and organize cake celebrations.

## Project Overview

Everyone deserves to celebrate their birthday with cake. This application is designed to track developer birthdays and manage cake days in the office. It consists of a Laravel backend and a Vue.js frontend.

The application takes as input a text file listing developers and their dates of birth, formatted as follows (one entry per line):

```
[Person Name],[Date of Birth (yyyy-mm-dd)]
```

For example:
```
Luna,2021-09-21
Freya,2024-01-20
```

The frontend displays upcoming cake days for the current year on a large screen in the office, so everyone knows when to expect cake. The UI, built with Vue and Tailwind, shows:

- Date
- Number of Small Cakes
- Number of Large Cakes
- Names of People Getting Cake

## Cake Day Rules

Cake days are determined by these rules:

- A small cake is provided on the first working day after an employee’s birthday.
- Employees get their birthday off.
- The office is closed on weekends, Christmas Day, Boxing Day, and New Year’s Day.
- If an employee’s birthday falls on a day when the office is closed, they get the next working day off.
- If multiple cake days fall on the same day, one large cake is provided to share.
- If there are cake days two days in a row, a large cake is provided on the second day.
- The day after any cake day must be cake-free for health reasons. Any postponed cakes are moved to the next working day.
- There is never more than one cake per day.

## Solution

The solution is a Vue.js frontend that consumes this Laravel API.

## Demo

You can see a working demo here: [Demo](https://vue.iamtechwriter.com/).  
The demo app is fully functional and connects to the Laravel API.

## Key Files

If you want to dive into the code, here are some important files:

- [CakeDaysResource.php](https://github.com/umernaeem/SoftDevAPI/blob/main/app/Http/Resources/CakeDaysResource.php)
- [CakeDaysController](https://github.com/umernaeem/SoftDevAPI/blob/main/app/Http/Controllers/Api/V1/CakeDaysController.php)
- [Api.php](https://github.com/umernaeem/SoftDevAPI/blob/main/routes/api.php)
