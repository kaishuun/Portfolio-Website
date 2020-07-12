+++
categories = ["Optimization"]
coders = []
date = 2020-07-10T23:00:00Z
description = "A Course Planning Optimization Model for the Operations Research Major Using Linear Programming"
github = ["https://github.com/kaishuun/Course-Planning-Optimization"]
image = "https://res.cloudinary.com/kevinhe/image/upload/v1594574598/MyatSFk0x6-inequality-constraints_r6ll99.png"
title = "Course Planning Optimization"
type = "post"

[[tech]]
logo = "https://res.cloudinary.com/kevinhe/image/upload/v1594574728/Microsoft_Office_Excel__282018_E2_80_93present_29_wgpihr.svg"
name = "Excel"
url = "https://www.microsoft.com/en/microsoft-365/excel"
[[tech]]
logo = "https://res.cloudinary.com/kevinhe/image/upload/v1594502945/1280px-LaTeX_logo.svg_ssv0z2.png"
name = "LaTeX"
url = "https://www.latex-project.org/"

+++
This is a quick overview of the project, to see the full write up, as well as the details of the mathematical model [click here](https://github.com/kaishuun/Course-Planning-Optimization/blob/master/project%20report.pdf)

## Introduction 

The Operations Research(OR) undergraduate program at Simon Fraser University(SFU) has one of the lowest amonut of students in comparison to other programs under the Faculty of Science. In a report by SFU, there were only 10 OR students in the program.

Due to histically low enrollments, as well as specific courses in OR, almost all required upper division courses are offered once per year or once per two years, making course planning very tedious for students in this major, especially if they are in the Cooperative Education program or other programs that SFU offers.

This project hopes to address this by using a Mixed Integer model to optimize the scheduling of courses and electives for students in this major

This portion will give a brief outlook on our report, to look at a detailed report of our findings, [click here](https://github.com/kaishuun/Course-Planning-Optimization/blob/master/project%20report.pdf), as well to look at our data and model formulation on Excel [click here](https://github.com/kaishuun/Course-Planning-Optimization/blob/master/Course%20Optimization.xlsx).

## Data Collection

All the required courses were collected from the SFU Student Services website. For this program, students have to complete their Lower Division, Upper Division, and Interdisciplinary Requirements.

To project courses, we went on each respective department website to get their projected courses for the upcoming two academic years. Data was gathered in this format:
![](https://res.cloudinary.com/kevinhe/image/upload/v1594525972/math_availability_qbmsyr.png)

This data was then combined to create this table of availibity, where on the left column are the required courses and the highlight cells representing that they are available in that semester

![](https://res.cloudinary.com/kevinhe/image/upload/v1594525780/Course_availability_n5gybk.png)

## Modelling 

Keeping in consideration of SFU graduatuation requirements, the OR major requirements, the next main focus would be looking at prerequisite courses. All upper division major courses have prerequesites, as an example STAT 350 has 3 prequesities, those being STAT 285, MATH 251, MATH 232 or 240. 
![](https://res.cloudinary.com/kevinhe/image/upload/v1594525337/course_description_dl1ozc.png)

To create this model we assign x<sub>i,j</sub> as course i being taken in the jth semester.
We also add more constraints such as, each course needed to be taken exactly once, having over 120 credits total, and taking less than 4 core courses in each semester to reduce the course load.

We also assign weights to each course depending on their year level (eg. MATH 408 would have a year 4 tag, while MATH 348 has a year 3 tag) to promote finishing required courses in their respective year. 
![](https://res.cloudinary.com/kevinhe/image/upload/v1594526982/course_weights_nkmgem.png)

## Results
We ran the Mixed Integer Program twice, once where no courses are allowed during the summer semester and one where courses are allowed in the summer semester. We conclude with the optimal scheduling for the OR Major as follows.

No Summer:

![](https://res.cloudinary.com/kevinhe/image/upload/v1594527231/optimal_schedule_-_1_qbicvr.png)

With Summer:

![](https://res.cloudinary.com/kevinhe/image/upload/v1594527231/optimal_schedule_-_2_iqlz8h.png)

Legend:

| Abbreviation  | Meaning       |
| ------------- |:-------------:| 
| UP-STAT | Upper-Division Statistics Cousrse
| INTR      | Interdiciplinary Course| 
| B-SOC      | Breadth- Social Science Course      | 
| B-HUM | Breadth- Humanities Course      | 
| ELEC | General Elective Course      | 

## Conclusion

Hope this project helps any incoming undergraduate Operations Research Students with course planning! Course planning is something that I do semesterly, as plans change due to Co-op of if courses clashes between the departments. To see a more in depth report, with the physical mathematical model described in detail [click here](https://github.com/kaishuun/Course-Planning-Optimization/blob/master/project%20report.pdf)

This report could also be found on the upcoming 2019-2020 Version of [Analytics Now](https://journals.lib.sfu.ca/index.php/analytics-now/index), an undergrduate journal of Operations Research.
