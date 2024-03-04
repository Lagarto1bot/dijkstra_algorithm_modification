## General info
This project modifies the classic Dijkstra algorithm in a way of adding another variable: vertex weights.
Not only do connection weights between vertices impact the final shortest routes, but also each vertex weight value changes how much speed we get from passing by it.
The idea came to my head when I attended a Discrete Mathematics course in the Mechatronics Faculty of Warsaw University of Technology.
I learned about graph theory and had to come up with a practical use of searching algorithms as part of a project.

## Technologies
Tools that were used:
* Python Notebook in Google Colab
* Numpy
* Heapq for heap usage

## Setup
To run this project you need to open it with any Python Notebook online editor or locally with preinstalled packages (Numpy ect.).

## Examples of use
Draw any graph in a form of adjacency list:
```python
graph = {
    'Sun': {'Proxima': 4.25, 'Ross': 11.01, 'Lalande': 8.31, 'Luyten': 12.35, 'Eridani': 10.5, 'Lacaille': 10.74, 'PM': 4},
    'Proxima': {'Sun': 4.25, 'Lalande': 6.58, 'Ross': 8.3, 'Lacaille': 13.8},
    'Lalande': {'Sun': 8.31, 'Luyten': 9.94, 'Ross': 3.22, 'Proxima': 6.58},
    'Ross': {'Sun': 11.01, 'Lalande': 3.22, 'Proxima': 8.3},
    'Luyten': {'Sun': 12.35, 'Eridani': 11.53, 'Lalande': 9.94},
    'Eridani': {'Sun': 10.5, 'Lacaille': 11.62, 'Luyten': 11.53, 'PM': 8.53},
    'Lacaille': {'Sun': 10.74, 'Proxima': 13.8, 'Eridani': 11.62, 'PM': 6.92},
    'PM': {'Sun': 4, 'Lacaille': 6.92, 'Eridani': 8.53}
}
```
In this case I used my local star system graph which includes an abstract concept of Przekaźnik Masy (Mass Relay)
that gives our space flight extra speed as if we used some massive star system for gravity assist. Other stars are
real and their distances are approximated.
Output of my algorithm:
```python
Najkrótsze ścieżki z systemu Sun: {'Sun': 0, 'Proxima': 4.25, 'Lalande': 8.31, 'Ross': 10.626546762589928, 'Luyten': 9.861657940663177, 'Eridani': 6.843333333333334, 'Lacaille': 6.306666666666667, 'PM': 4.0}
```
It prints calculated time of our journey and shows that using gravity assist or passing by Mass Relay is efficient way to travel around the system.

## Future improvements
I'm planning on adding more visualization and print each step of shortest routes for clarity.
