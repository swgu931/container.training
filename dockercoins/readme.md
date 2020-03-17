# Docker Coins

 : https://training.play-with-kubernetes.com/kubernetes-workshop/


## What’s this application?
- It is a DockerCoin miner! 💰🐳📦🚢
- No, you can’t buy coffee with DockerCoins
- How DockerCoins works:
  .worker asks to rng to generate a few random bytes
  .orker feeds these bytes into hasher
  -- and repeat forever!
  -- every second, worker updates redis to indicate how many loops were done
  -- webui queries redis, and computes and exposes “hashing speed” in your browser


-rng = web service generating random bytes
-hasher = web service computing hash of POSTed data
-worker = background process using rng and hasher
-webui = web interface to watch progress

