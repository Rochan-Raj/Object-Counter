# object_Counter

## Description:
In this project, I created an object counting system based on Computer Vision (CV).

Now, the question is this CV?

Computer Vision is an interdisciplinary field concerned with giving computers the ability to “see” or be able to understand the contents of digital images such as photos and videos. While vision is a trivial task for humans and animals, it’s currently quite difficult for machines. However, a lot of progress has been made in the field in the last few decades and new techniques and technologies to make CV faster and more accurate are actively being researched.

An object counting system, as you might have already inferred, is a system that counts and tracks objects on a definite path. Why would you want to build one? Why would you want to count objects on the path? 

Well, if I talk about specifically, vehicles on a road we can do the following useful things: 

•	Traffic management and planning: If you have a good sense of the volume of traffic moving along a given road or network of roads, you can better understand congestion and then manage and/or make plans to reduce/eliminate it. Vehicle count data is very useful to urban city planners and transport authorities.

•	Traffic control: No one likes to be stuck behind a red light especially when the road is free. Vehicle counting systems can be integrated with traffic light control software to intelligently direct vehicles based on the current traffic situation in real-time.

•	Parking management: A VCS can be installed at the entrance of a parking lot to monitor vehicles coming in and going out to determine whether there are slots available at any given time. It can also be used to ensure the number of vehicles in a given place (such as a hotel or events center) does not exceed its capacity by controlling Automatic Barrier Gates as opposed to issuing tags.

•	Advertising: Billboard advertisers and their clients are interested in the volume of vehicular traffic along a road where they have ads or where they want to install a billboard because they can make estimates of the number of people who see their ads per time using the data.

## How it works

The object counting system I built is made up of three main components: 

•	Detector:
The detector identifies an object in a given frame of video and returns a list of bounding boxes around the objects to the tracker. The detector is also used to update the trackers periodically to ensure that they are still tracking the objects correctly.

•	Tracker:
The tracker uses the bounding boxes to track the vehicles in subsequent frames.

•	Counter:
The counter counts objects when they leave the frame or makes use of a counting line drawn across a road.


## Background subtraction

The first detector I used to identify an object was a background subtractor. Background or image subtraction is the process of extracting the foreground of an image from its background. If you have a background image like a road without vehicles in it, you can subtract this image from another image of the same road (from the same view) which contains vehicles to detect those vehicles. The background pixels would cancel each other out and the objects in the foreground would pop out.

The images below show what background subtraction looks like.

![image](https://user-images.githubusercontent.com/85439772/189491939-1578c4a8-b117-42b4-8aeb-1487e259fb43.png)


![image](https://user-images.githubusercontent.com/85439772/189491413-828be8a9-e2b4-48f8-8b2e-ed8cb232cb02.png)

![image](https://user-images.githubusercontent.com/85439772/189491960-63ca48b3-97ce-4069-bf40-7821acd95bc0.png)

![image](https://user-images.githubusercontent.com/85439772/189491967-b5582a1f-fe96-4b4a-a457-1f41f9926e38.png)


## Deep Sort For Vehicle tracking

Deep Sort Algorithm involves tracking of the objects using Kalman Filters, Association of new detections and new predictions using the Hungarian Algorithm and using Appearance vector for better predictions. So let's dive into all these concepts.

## Modules used
•	OpenCV

•	Numpy

## Demo

https://user-images.githubusercontent.com/85439772/189491584-9566496f-a6fe-450e-8ade-99993c5c2111.mp4



https://user-images.githubusercontent.com/85439772/189491881-939e8249-b0d5-4fcf-aa0d-60669cadd709.mp4



## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

