# Docker Coins

 : https://training.play-with-kubernetes.com/kubernetes-workshop/
 : https://github.com/dockersamples/dockercoins


## What’s this application?
- It is a DockerCoin miner! 💰🐳📦🚢
- No, you can’t buy coffee with DockerCoins
- How DockerCoins works:

  .worker asks to rng to generate a few random bytes

  .worker feeds these bytes into hasher
  
  .and repeat forever!
  
  .every second, worker updates redis to indicate how many loops were done
  
  .webui queries redis, and computes and exposes “hashing speed” in your browser


- rng = web service generating random bytes
- hasher = web service computing hash of POSTed data
- worker = background process using rng and hasher
- webui = web interface to watch progress

## Getting the application source code

- git clone https://github.com/dockersamples/dockercoins
- cd ~/dockercoins
- Use Compose to build and run all containers:
  
  $docker-compose up
  
  : Compose tells Docker to build all container images (pulling the corresponding base images), then starts all containers, and displays aggregated logs.


