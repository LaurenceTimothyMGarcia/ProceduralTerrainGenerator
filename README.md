# Unity Procedural Terrain Generator
 Procedural Terrain Generator using Perlin Noise. Currently working on adding more features that allow for mazes and a stronger shader system.

 This is a separate repository from [Gunslinger Hilda](https://github.com/LaurenceTimothyMGarcia/GunslingerHilda) in order to segment the tool from that specific game prototype.

# Description
An isolated build of a procedural terrain generator tool for Unity. The tool builds a 2D perlin noise texture then uses the terrain mesh to determine the height of each pixel on the map. Separating the tool into these 2 components allows the user to have more control over the individual components. This tool is based on Sebastian Lague's Procedural Generation Series.

Additional features such as connected maze generation with and flood fill algorithms to identify segments are implemented but need some optimization.

# Install
* Download the [**Unity Package**](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/ProcGenTerrainScene.unitypackage)
* Or clone/download the repo

# Breakdown
You can create 2 Scriptable Objects that you will attach to the MapGenerator.

## Noise Generator
Users can edit the noise map to fit their needs.

![Noise Generator](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Instructions/NoiseTool.png)

### Details of the map
Noise Scale, Octaves, Persistance, Lacunarity allow for the user to edit the overall and finer details of each terrain. 

### Seeds
Users can also set specific seeds to save instances of terrains for their respective project.

## Terrain Generator
Users can edit the rules of what type of terrain is generated through the noise map.

![Terrain Generator](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Instructions/TerrainTool.png)

### Height of Mesh
Mesh height can be determined by the multipler and the height curve.

### Falloff Map
If terrain is not endless, they can have a fall off which users can use to create things such as mountains or islands.

## Images
![Terrain Generation Iteration 1](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Examples/Terrain%20Generator%20Iteration%201.png)
![Terrain Generation Iteration 2](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Examples/Terrain%20Generator%20Iteration%202.png)
![Terrain Generation Iteration 3](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Examples/Terrain%20Generator%20Iteration%203.png)
![Terrain Generation Iteration 4](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Examples/Terrain%20Generator%20Iteration%204.png)
![Terrain Generation Iteration 5](https://github.com/LaurenceTimothyMGarcia/ProceduralTerrainGenerator/blob/main/Assets/Images/Examples/Terrain%20Generator%20Iteration%205.png)

# Future Additions
* The current shader system is a bit limited and users have to interact directly with the shader nodes. Goal in the future is to make this easily accessible from the inspector.
* Optimize the maze pathfinding and the flood fill algorithm to have faster load times when using those respective features.
* Add different noise options to allow for more types of terrain and maps.

# Used in Projects
## **Gunslinger Hilda**
Used in a rogue like context to build new maze canyons every time the player starts a new run.
* [Itch.io Page](https://emergencyplayer.itch.io/gunslinger-hilda)
* [Github Page](https://github.com/LaurenceTimothyMGarcia/GunslingerHilda)