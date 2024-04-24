<p align="right">15 𝘮𝘪𝘯𝘶𝘵𝘦 𝘳𝘦𝘢𝘥 📚 </p> <br>

<p align="center">
  <img src="readme_data//carla_apollo.png" alt="Project Logo Cover" width="1111"/>
</p>

# Project Overview

Apollo is owned by GuardStrikeLab.

# A) Official Links and Repositories

- **GuardStrikeLab GitHub**: [Apollo Main Repository](https://github.com/guardstrikelab)
- **Carla Apollo Bridge Details**: [CARLA and Apollo Integration](https://carla.org/2022/11/28/carla-apollo-bridge/)
- **Carla Apollo Bridge Repository**: [GitHub Repo](https://github.com/guardstrikelab/carla_apollo_bridge)
- **Apollo Repository**: [GitHub Repo](https://github.com/guardstrikelab/apollo)

# B) Complete Setup Instructions

For a comprehensive guide on setting up the Apollo-Carla integration, refer to the detailed documentation provided by MaisJamal. The repository contains all necessary instructions and resources:

- **MaisJamal's Repository**: [Carla-Apollo Bridge Setup](https://github.com/MaisJamal/carla_apollo_bridge.git)

# C) Instructions to start the entire software stack

### Terminal 1: Apollo Docker and DreamView

#### 1.1 Start Apollo Docker Container
Initiate the Apollo Docker container with the following command:
```bash
bash docker/scripts/dev_start.sh
```

#### 1.2 Attach to Docker Container
Connect to the running Apollo Docker container:
```bash
bash docker/scripts/dev_into.sh
```

#### 1.3 Build Apollo (Only Required Once)
Compile Apollo with GPU support:
```bash
./apollo.sh build_gpu
```

### Terminal 2: Carla Docker

#### 1.4 Start Carla Simulator
Start the Carla simulator with the following docker command:
```bash
docker run -it --privileged -v /tmp/.X11-unix:/tmp/.X11-unix:rw -v /usr/lib/nvidia:/usr/lib/nvidia --device /dev/dri --rm -e __NV_PRIME_RENDER_OFFLOAD=1 -e __GLX_VENDOR_LIBRARY_NAME=nvidia -e DISPLAY=$DISPLAY -e NVIDIA_VISIBLE_DEVICES=all -e NVIDIA_DRIVER_CAPABILITIES=all --gpus=all --name=carla-server --net=host -d carlasim/carla:0.9.13
```

#### 1.5 Build Carla Docker (Only Required Once)
Navigate to the `docker` directory and build the Docker container:
```bash
cd docker
./build_docker.sh
```

#### 1.6 Run Carla Docker
Execute the Docker run script:
```bash
./run_docker.sh
```

#### 1.7 Enter Docker Container
Access the running Carla Docker container:
```bash
docker exec -ti carla-apollo-13 bash
```

#### 1.8 Change Working Directory
Navigate to the main working directory inside the container:
```bash
cd ~/carla_apollo_bridge_13/
```

#### 1.9 Run Carla Simulator
Start the Carla simulator:
```bash
python carla-python-0.9.13/util/config.py -m Town01 --host 172.17.0.1
```

#### 2.0 Start Carla Manual Control
Run manual control to interact with the simulator:
```bash
python examples/manual_control.py
```

#### 2.1 Start the Carla-Apollo Bridge
Facilitate communication between Carla and Apollo:
```bash
python carla_cyber_bridge/run_bridge.py
```

#### 2.2 Start Dreamview
Launch the Dreamview web interface:
```bash
bash scripts/bootstrap.sh
```

#### 2.3 View Dreamview
Access Dreamview in a web browser at:
```plaintext
http://localhost:8888/
```

#### 2.4 Change the Map or Spawn Traffic
Modify the simulation environment:
```bash
python carla-python-0.9.13/util/config.py -m Town04 --host 172.17.0.1
python examples/generate_traffic.py --async
```

<hr> 

### Closing Sessions

#### Closing Docker Containers

#### Stop Dreamview
Shut down Apollo Dreamview:
```bash
bash scripts/bootstrap.sh stop
```

#### Properly stop and remove Docker containers after use:

```bash
# Stop the Carla and Apollo containers
docker stop carla-server apollo_dev_radhakrishna

# Remove the containers
docker rm carla-server apollo_dev_radhakrishna
```

<hr><br><br>
<p align="center">
  <img src="readme_data//HKAD_quote.png" alt="Project Logo Cover" width="1111"/>
</p>




