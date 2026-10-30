MiniGrid MultiRoom: Room-Size and Grid-Size Comparison
Overview
This notebook compares two configurations of the MiniGrid MultiRoom environment:
- Original room-size setting: maxRoomSize=4
- Enlarged-room setting: maxRoomSize=10
Both configurations use the environment ID MiniGrid-MultiRoom-N2-S4-v0, the same random seed (42), and the same configured overall map dimensions (25 x 25).
The notebook displays the two generated environments side by side and prints the map dimensions, configured maximum room size, and room dimensions exposed by the installed MiniGrid version.


Requirements
Install the required Python packages before running the notebook:
pip install gymnasium minigrid matplotlib

How to Run
1. Open Compare_grid_size.ipynb in Jupyter Notebook, JupyterLab, or Visual Studio Code.
2. Make sure the required packages are installed in the selected Python environment.
3. Run the code cell.
4. Review the side-by-side environment images and the printed room/map information.
5. The code saves the comparison figure as grid_size_comparison.png in the notebook's current working directory.

Configuration Details
Parameter	Original configuration	        Enlarged-room configuration
Environment	MiniGrid-MultiRoom-N2-S4-v0	MiniGrid-MultiRoom-N2-S4-v0
maxRoomSize	          4	                        10
width	                 25	                        25
height	                 25	                        25
Random seed	         42	                        42


Important Notes
- maxRoomSize sets the maximum room-size parameter passed to the environment. It does not guarantee that every generated room will be larger.
- width=25 and height=25 configure the overall environment map dimensions.
- The Matplotlib figure size (figsize) and resolution (dpi) affect only the displayed or saved image. They do not change the MiniGrid environment or its grid dimensions.
- Check the printed room dimensions and the generated image before concluding that the actual rooms are larger.

Scope of This Experiment
This notebook demonstrates an environment configuration and visual layout comparison. It does not measure reinforcement-learning performance or prove that an agent learns better in the enlarged-room configuration. That would require training or evaluating the agent in both configurations and comparing consistent metrics, such as success rate, episode length, and reward.

Reproducibility
Both configurations use seed 42. Exact layouts and the availability/format of room-dimension information may vary across MiniGrid versions. For reproducible results, record the Python and package versions used for the experiment.