# Elective Project:  
# Functional Safety of a Lane Assistance System

## Hazard Description:
There are four hazards covered in Hazard Analysis and Risk Assessment (HARA) document.  
Two hazards are given, and some part of analysis is discussed in Udacity lessons.  
The technical details of other two are important because they assume some uncommon geographic conditions.  

Thus, the detail will be covered in separate README's.  
You may just skip to the documents if you feel like TL;DR.

### HA-003 Possible camera malfunction at a tunnel
This particular issue has been in my mind for years, long before I take self-driving car nanodegree program.

https://github.com/na6an/sdcnd-t3/blob/master/P2_Elective-Functional_Safety/HA-003.md

In this project, I will just simplify the requirements for this issue by addressing an artificial variables,  
Lumen_Change and Lumen_Frequency. (* Lumen is a physics unit of luminous flux)

### HA-004 ECU malfunction (off real-time due to ECU overheating)
https://github.com/na6an/sdcnd-t3/blob/master/P2_Elective-Functional_Safety/HA-004.md

For this issue, I assumed there is a variable that measures ECU temperature, Temp.

## Scope of This Project:
Two hazards added in HARA were covered partially in Technical Safety Concept for simplicity of the project.  
Also, Software Requirement and Architecture discusses Functional Safety Requirement 01-01 only.
