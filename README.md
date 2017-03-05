# OnlineVideoChallenge
Online Video Takehome Challenge. From *A Collection of Data Science Takehome Challenges* by Guilio Palombo.

## Challenge Description

Company XYZ is an online video streaming company, just like YouTube or Dailymotion. The Head of Product has identified as a major problem for the site a very high home page dropoff rate. That is, users come to the home-page and then leave the site without taking any action
or watching any video. Since customer acquisition costs are very high, this is a huge problem: the company is spending a lot of money to acquire users who don't generate any revenue.Currently, the videos shown on the home page to new users are manually chosen. The Head of
Product had this idea of creating a new recommended video section on the home page.

He asked you the following:
- Classify each video into one the 3 categories below and explain your approach:
  - "Hot" - means trending up. These videos are candidate to be shown.
  - "Stable and Popular" - video view counts are flat, but very high. These videos are candidates to be shown too.
  - "Everything else" - these videos won't be shown.
- What are the main characteristics of the "hot videos"?
- After having identified the characteristics of the hot videos, how would you use this information from a product standpoint?

## Data
We have two tables:
- video_count - provides information about how many times each video was seen by day. Columns:
  - **video_id**: video id, unique by video and joinable to the video id in the other table
  - **count**: total count of views for each video by day
  - **date**: on which day that video was watched that many times
- video_features - characteristics of the video. Columns:
  - **video_id**: video id, unqiue by video and joinable to the video id in the other table
  - **video_length**: length of the video in seconds
  - **video_language**: language of the video, as selected by the user when she uploaded the video
  - **video_upload_date**: when the video was uploaded
  - **video_quality**: quality of the video. It can be [ 240p, 360p, 480p, 720p, 1080p]
