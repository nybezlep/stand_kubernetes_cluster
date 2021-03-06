# Demo stand. Model: squad_ml

## Building and running with Docker:
[Nvidia-docker](https://github.com/NVIDIA/nvidia-docker) container runtime required to run this image.

1. If necessary, build base docker_cuda and docker_deeppavlov images for CUDA 9.0 from:

   https://github.com/deepmipt/stand_docker_base
  
2. Go to the `stand_kubernetes_cluster/models/stand_squad_ml` directory

3. Build Docker image:
   ```
   sudo docker build -t stand/squad_ml .
   ```
4. Run Docker image:
   ```
   sudo docker run -p <host_port>:5000 --runtime=nvidia --device=/dev/nvidia<gpu_unit_int_id> -v /path/to/host/vol/map/dir:/logs stand/squad_ml
   ```

# License

Apache 2.0 - licensed.