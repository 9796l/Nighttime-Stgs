# Double Decomposition for Nighttime Driving Scene Simulation
1. Clone our Repo:
   ```Bash
   git clone https://github.com/Jingyang06/DD-NightSim.git --recursive
   ```
2. Installation:
```Bash
  conda create -n nighttime-stgs python=3.8
  conda activate nighttime-stgs

  pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cu118

  # Install requirements
  pip install -r requirments.txt

  # Install submodules
  pip install ./submodules/diff-gaussian-rasterization
  pip install ./submodules/simple-knn
  pip install ./submodules/simple-waymo-open-dataset-reader
  python script/test_gaussian_rasterization.py
  ```
3. Prepare for dataset:
   We use nighttime waymo dataset following [EmerNeRF](https://github.com/NVlabs/EmerNeRF/blob/main/docs/NOTR.md)
4. Training:
   ```Bash
   bash script/waymo/train_waymo_exp.sh
   ```
5. Rendering:
   ```Bash
   bash script/waymo/render_waymo_exp.sh
   ```
   
