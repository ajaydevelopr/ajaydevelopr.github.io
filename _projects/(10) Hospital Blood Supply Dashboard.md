---
name: Blood Supply Predictor
tools: [shiny-app]
image: https://raw.githubusercontent.com/athan-dial/athan-dial.github.io/gh-pages/_data/project_files/machacks.png
description: A small web app built for a clinical purpose with Shiny
---

<h1> Context </h1>
 This app was part of a hackathon I participated in - MacHacks 2021.
 My team and I ventured to optimize the blood supply in a hospital setting.
 This is a very relevant problem in many hospitals for a few reasons:
 <br>
 <br>

1. Blood products have varying shelf lives, as long as 1 year, and as short as 12 days, depending on which fraction of the blood it is.</br>
2. Hospitals are constantly having to balance the intake of new donations with the predicted demand for transfusions in the future. Inefficiency in the inventory management of a hospital can lead to the loss of hundreds of units of blood per year. </br>

<h1> Idea </h1>
Our teams idea was to create an automated end-to-end predictive modelling system that would be able to inform physicians and hospital staff when they would need blood, how much, and what type of blood they would need.

<h1> Approach </h1>

I was responsible for the development of the front and backend of the app, including the development of a synthetic dataset that modelled the important parameters of a blood bank database.

<h1> Result </h1>
The app can be found on [my shiny dashboard](https://athan-dial.shinyapps.io/blood_supply_predictor/ "Blood Supply Predictor"). The source code is available at [my github](https://github.com/athan-dial/mackhacks_2021 "github.com/athan-dial"). You can view the 5-minute video submission created by my team and I on Youtube.
<br>
<br>
<div href="http://www.youtube.com/watch?feature=player_embedded&v=VSwHVP7l3ww
" target="_blank"><img src="http://img.youtube.com/vi/VSwHVP7l3ww/0.jpg"
alt="Blood Supply Predictor" width="480" height="360" border="10" /></div>


<h1> [Under development] </h1>
As this was part of a very rapid ~6 hour prototyping period, I would not say the product is finished. The goal was to get an app that *worked* in with the proposed data in that time. As such, I would still like to add an actual predictive model to the backend to better reflect the full goal for the project.
