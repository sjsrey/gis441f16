## GIS 441 Fall 2016
## Geographics: Interactive and Animated Geovisualization


----------

### Instructor


|Dr. Sergio J. Rey | [www](https://geoplan.asu.edu/sergio-rey)
|:-------- |:------
|Office    |  Coor 5612
|Hours     | Tuesdays 14:00-15:00 or by appointment
|email     | [Sergio.Rey@asu.edu](mailto:Sergio.Rey@asu.edu)


### Meeting Logistics

|Lecture   | Times
|:-------- |:------
|Coor 5505 | Tu,Tr 12:00-13:15


----------



## Introduction
This course will introduce the concepts and theories of animated-interactive cartography and geovisualization in a computationally based manner. To support the latter a major component of the course will rely on several new visualization and mapping technologies for the web including cartopy (Python), Folium (Python), D3 (JavaScript) and Bokeh (Python),  among others.  In addition to a series of in-class exercises that introduce these technologies, students will apply their newly acquired technical skill sets to a final project in exploratory geovisualization.

## Objectives

1. Introduction to basic theory in cartography and geovisualization
2. Introduction to the application of geovisualization to different research domains
2. Acquire computational skills  for rapid prototyping of effective data visualizations
3. Experience in designing, implementing, and testing an empirical project that combines core theory with software development

## Prerequisites
1. Interest in geovisualization
2. A grade of B or better in [GIS 321 Programming for GIS](https://github.com/jlaura/GIS321/blob/master/syllabus.md) (or comparable)


## Grading

### Student Led Discussion

Each student will prepare a presentation on one of the key conceptual areas of the course to be presented to the group. Lead readings for each topic will be assigned at the beginning of the semester and each student leading a particular discussion is expected to research and include additional readings on that topic. This component of your course grade is based on 15 possible points.  

### Quizzes

Quizzes  will be based on the textbook, assigned videos, and course discussions. These will be given during the first five minutes of class on the Thursdays beginning on week 2, Aug 25, through Oct 6.  There are not makeups for the quizzes. Quizzes are graded on a pass(5)/fail(0). Your overall quiz grade will be based on a maximum of 25 points .

### Project 
The capstone of GIS441 will be a final project that integrates the theoretical and conceptual materials from the first half of the course together with your newly acquired technical skill sets.  Students will work on an individual project with the instructor as a collaborator to provide feedback and guidance as the project evolves. All projects will be presented on the date of the final. A short (2000-2500 words) paper describing the substantive topic and the development of the application are required. Full source code and data to reproduce the visualization must also be submitted on GitHub.  Details on the project will be given out in Week 3 of the semester.

### Participation

The success of a course is highly dependent upon the active engagement of students as well as their collaboration with their peers. Each student's participation in the course will be evaluated on a 5 point scale.  Participation can take many forms, from bringing new materials into discussion, posing interesting questions, pair programming with a colleague to help them on their project as well as suggestions for improving the course.  

### Final Grade

| Component     | Points |
|---------------|-------:|
| Discussion    |     15 |
| Quizzes       |     25 |
| Project       |     55 |
| Participation |      5 |

Course final letter grades will be assigned as follows:

Letter | Points
------ | ----------
A+     |[97-100]
A      |[93-96]
A-     |[90-92]
B+     |[87-89]
B      |[83-86]
B-     |[80-82]
C+     |[77-79]
C      |[70-76]
D      |[60-69]
E      |[0-59]        


## Computational Resources

All the software we will be using during the semester is [open source](https://opensource.com/resources/what-open-source).  **You are strongly encouraged to bring your own laptops to class to install these packages**. As a bring your own device (BYOD) course, this will allow you to more fully explore the software and work outside of dedicated class time. We will cover the installation of the packages in the early part of the semester.  

## Readings
Slocum, T.A., R.B. McMaster, F.C. Kessler and H.H. Howard (2009)Thematic Cartography and Geovisualization. Prentice Hall, Upper Saddle River.

## Schedule

The course is organized into two  parts. In order to be able to develop your own geovisualizations it is vital that you first acquire basic software development skills together with a grounding in the domains of cartography and geovisualization. In Part I  we will cover fundamental concepts of cartographic theory and geovisualization on Tuesdays and then on Thursdays we will explore particular Python libraries that relate to each theoretical concept, and that can form key components of course projects. Part II  shifts to a studio format where we will focus on project based learning. Here you will apply your newly acquired (or enhanced) development skills to an empirical project developing a geovisualization product. This second part will also include additional theoretical and methodological concepts as needed.  


| Week  | Date  | Topic                          | Due                       |
|-------|-------|-------------------------------------------------------|---------------------------|
| 1     | 8.18  | Course Introduction            |                           |
| 2     | 8.23  | [Geovisualization](/content/geovisualization.rst)               |                           |
|       | 8.25  | [PySAL for Geographical Data Science](https://youtu.be/TY4QWnnd4jY) | Quiz 1                    |
| 3     | 8.30  | [Projects Overview](/content/projects.md)         |                           |
|       | 9.1   | Software Installation     | Quiz 2                    |
| 4     | 9.6   | Spatial Data Formats      | Project Selection         |
|       | 9.8   | Geoprocessing with PySAL  | Quiz 3                    |
| 5     | 9.13  | [Data Classification Ch 3, 4][class]       | Discussion 1              |
|       | 9.15  | PySAL Classifiers         | Quiz 4                    |
| 6     | 9.20  | [Color and Symbolization Ch 5, 10][class]   | Discussion 2              |
|       | 9.22  | palletable                | Quiz 5                    |
| 7     | 9.27  | [Multivariate Maps Ch 18][class]        | Discussion 3              |
|       | 9.29  | cartopy                   | Quiz 5                    |
| 8     | 10.4  | [Interactivity  Ch 21, 22][class]           | Discussion 4              |
|       | 10.6  | bokeh                     | Quiz 6                    |
| 9     | 10.11 | *Fall Break*              |                           |
|       | 10.13 | Requirements Analysis     |                           |
| 10    | 10.18 | Requirements Analysis     |                           |
|       | 10.20 | Project Design            | Analysis Document         |
| 11    | 10.25 | Project Design            |                           |
|       | 10.27 | Prototype Development     | Design Document           |
| 12    | 11.1  | Prototype Development     |                           |
|       | 11.3  | Prototype Development     |                           |
| 13    | 11.8  | Prototype Development     |                           |
|       | 11.10 | Prototype Development     |                           |
| 14    | 11.15 | Testing                   |                           |
|       | 11.17 | Testing                   |                           |
| 15    | 11.22 | Product Implementation    | Testing Report            |
|       | 11.24 | *Thanksgiving Holiday*    |                           |
| 16    | 11.29 | Product Implementation    |                           |
|       | 12.1  | Product Implementation    |                           |
| Final | 12.6  | Presentation              | Final Code/Documentation  |

## Policies

 - You are expected to attend all classes and participate in the hands-on instruction
 - You are expected to work on the materials after the hands-on sessions as well
 - Office hours will not be used to cover material you missed due to an absence
 - No makeups for missed quizzes or deadlines will be given.

### Academic integrity
The ASU student academic integrity policy lists violations in detail. These violations fall into five broad areas that include but are not limited to: cheating on an academic evaluation or assignment, plagiarizing, academic deceit, such as fabricating data or information, aiding academic integrity policy violations and inappropriately collaborating, or falsifying academic records. For more information about the ASU student academic integrity policy, please use the following web link
http://provost.asu.edu/academicintegrity

### Code of Conduct
As course instructor, I am dedicated to providing a harassment-free learning experience for all students, regardless of gender, sexual orientation, disability, physical appearance, body size, race, religion, or choice of operating system.  All course participants are expected to show respect and courtesy to other students  throughout the semester.  As a learning community we do not tolerate harassment of participants in any form.

All communication should be appropriate for a professional audience including people of many different backgrounds. Sexual language and imagery is not appropriate in this course.

Be kind to others. Do not insult or put down other students. Behave professionally. Remember that harassment and sexist, racist, or exclusionary jokes are not appropriate for GIS441.

Students violating these rules may be asked to leave the course, and their violations will be reported to the ASU administration.

This code of conduct is an adaptation of the [SciPy 2016 Code of Conduct](http://scipy2016.scipy.org/ehome/146062/388087/).

### Disability accommodations
Qualified students with disabilities who will require disability accommodations in this class are encouraged to make their requests to me at the beginning of the semester either during office hours or by appointment. Note: Prior to receiving disability accommodations, verification of eligibility from the Disability Resource Center (DRC) is required. Disability information is confidential.



[q1]: https://myasucourses.asu.edu/webapps/blackboard/content/launchAssessment.jsp?course_id=_338703_1&content_id=_14242344_1&mode=cpview
[class]: http://library.lib.asu.edu/search~S3?/pr/pr/1,36,60,B/frameset~4573787&FF=prey+s&1,1,
