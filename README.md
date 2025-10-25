# Week 5 Task – OpenROAD Flow Setup and Floorplan + Placement

## Install OpenROAD Flow Scripts

1. clone the repo with submodules
   
   ```bash
   git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts
   cd OpenROAD-flow-scripts
   ```
   
    ![](assets/2025-10-21-10-02-10-image.png)

2. run setup script with root permissions, 
   
   ```bash
   sudo ./setup.sh
   ```
   
   ![](assets/2025-10-21-20-29-59-image.png)

3. Build OpenROAD
   
   ```shell
   ./build_openroad.sh --local --threads 1
   ```
   
   ~~NOTE: The local build failed so i resorted to using prebuilt binaries from [Using Pre-built Binaries &#8212; OpenROAD Flow documentation](https://openroad-flow-scripts.readthedocs.io/en/latest/user/BuildWithPrebuilt.html)~~
   
   ![](assets/2025-10-25-14-17-23-image.png)



4. verifying installation
   
   ```shell
   source ./env.sh
   yosys -V  
   openroad -version
   ```
   
    ![](assets/2025-10-25-14-16-57-image.png)

## Execute Floorplan and Placement

### Create floorplan

```
make DESIGN_CONFIG=./designs/sky130hd/vsdbabysoc/config.mk floorplan
```

![](assets/2025-10-25-14-47-51-image.png)


