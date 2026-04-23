# Physarum Dynamic Routing Simulation(PDRS)

Developed by Jip S. Heimeriks as part of an Artificial Intelligence bachelor thesis at Utrecht University

## Simulation Goals
The Physarum Dynamic Routing Simulation (PDRS) is a simulation designed to evaluate the performance of the **Improved Physarum Polycephalum Algorithm (IPPA) by Zhang et al.**[1] when it is utelized to find evacuation routes in environments affected by dynamically spreading wildfires. The simulation is additionally equipped with another path-finding algorithm, **Dijkstra's algorithm** [2], to provide a comparison with a widely used algorithm.

### Key Features
*   **Real-World road networks:** The **OSMnx library** is used to download real road network data from **OpenStreetMap** [3].
*   **Dynamic Wildfires:** A cellular automata model based on the model by **Alexandridis et al.**[4] was implemented, simulating spreading wildfire.
*   **Physarum algorithm:** IPPA is utelized to find evacuation routes from the village to the safe exits trough the hazardous wildfire environment. IPPA is able to identify multiple alternative evacuation routes to various exits simultaneously, mimicing the properties of the one celled organism it is inspired by.
*   **Comparative Analysis:** Dijkstra’s algorithm is employed similarly to find evacuation routes. This algorithm is included as a comparitive measure to the IPPA algorithm. The algorithms are compared on robustness and efficiency.

## Using the Simulation
The simulation is written in **Python** using **Jupyter Notebook**.
The notebook can be opened in Colab  with the folowing link: [![Open In Colab](https://githubtocolab.com/jipheimeriks/Physarum-Dynamic-Routing-Simulation)](https://githubtocolab.com/jipheimeriks/Physarum-Dynamic-Routing-Simulation)
Alternatively it can be opened in Jupyter Notebook,
therefore Anaconda and Jupyter must be installed via: [![Download Anaconda](https://www.anaconda.com/download)](https://www.anaconda.com/download) 
The notebook can be opened with Visual Studio Code as well. Make sure to download the .ipynb code, additionally make sure that Visual Studio Code is installed on your device. 

### Requirements
Ensure you have the following Python libraries installed:
*   `osmnx`
*   `numpy`
*   `matplotlib`
*   `networkx`

### Implementation details 
Details of the implementation can be found inside the notebook. 
There an overvieuw of all model parameters can be found. 

## Research Context
This simulation was designed for a bachelor thesis. The aim of the thesis was to address the need for evacuation models that account for the dynamic nature of wildfires. After a number of experiments were conducted it was foud that, while Dijkstra remains more efficient, the Physarum model provides a critical advantage in its inherent ability to find multiple alternative escape routes simultaniously, which may mitigate traffic congestion during real-world evacuations.

## Sources of the adapted models

The wildfire simulation in the PDRS is based after:
"A cellular automata model for forest fire spread prediction: The case of the wildfire that swept through Spetses Island in 1990". Alexandridis, A. et al. https://doi.org/10.1016/j.amc.2008.06.046
and
"Wildland fire spread modelling using cellular automata: evolution in large-scale spatially heterogeneous environments under fire suppression tactics". Alexandridis, A. et al.https://doi.org/10.1071/wf09119

The Physarum algorithm used in the PDRS is based after:
An Improved Physarum polycephalum Algorithm for the Shortest Path Problem. Zhang, X. et al. https://doi.org/10.1155/2014/487069

The Dijkstra algorithm used in the PDRS is based after:
A note on two problems in connexion with graphs. Dijkstra, E.
https://doi.org/10.1007/bf01386390
