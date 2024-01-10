[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12143268&assignment_repo_type=AssignmentRepo)
# Astro 528 [Class Project](https://psuastro528.github.io/Fall2023/project/)

[![](https://img.shields.io/badge/docs-stable-blue.svg)](https://PsuAstro528.github.io/project-template/stable)

GitHub Actions : [![Build Status](https://github.com/PsuAstro528/project-template/workflows/CI/badge.svg)](https://github.com/PsuAstro528/project-template/actions?query=workflow%3ACI+branch%3Amain)


## Project Goals:  
- Create an N-body simulator of the solar system
- Utilize GPU acceleration

## Overview

This project takes data from the NASA JPL Horizons Database on Solar System objects. The code calculates the acceleration from the position, velocity, and masses of the objects. This is then integrated through time using the Leap Frog algorithm. This is then compared against NASA JPL Horizon's data for the date the simulator has been integrated to. 

This test is repeated for varying step sizes and integration times.

## File Breakdown

- main.jl has main code that integrates all others
- get_planet_data.jl downloads planet data from JPL horizons
- physical_eqns.jl obtains velocity and acceleration data given positions and velocity
- Leap_Frog.jl integrates system using Leap Frog algorithm
  
## To Do List:
- Figure out how to efficiently parse through JPL Horizons
- Perform integrations on the data
- compare the final integration state to actual data
- Repeat above for various step sizes and integration times
- create fully fleshed tests
- input more assertions for reality checks in methods
- implement more solar system objects than just the planets as to have a significant difference between tests

## Class Project Schedule
- Project proposal (due Sept 6)
- Serial version of code (due Oct 2)
- Peer code review (due Oct 9)
- Parallel version of code (multi-core) (due Oct 30)
- Second parallel version of code (distributed-memory/GPU/cloud) (due Nov 13)
- Completed code, documentation, tests, packaging (optional) & reflection (due Nov 29)
- Class presentations (Nov 27 - Dec 6, [detailed schedule](https://github.com/PsuAstro528/PresentationsSchedule2023) )

