# Arma III

## How to use this image?

```bash
docker run -it \
	--env-file credentials \
	-v $PWD/arma3:/arma3 \
	-v $PWD/profiles:/profiles \
	-p 2302:2302 \
	-p 2303:2303 \
	-p 2304:2304 \
	-p 2305:2305 \
	houki/arma3
```

## Sample `credentials` file

```
STEAM_USERNAME=your_steam_username
STEAM_PASSWORD=your_steam_password
```

## Custom mission

```bash
docker run -it \
	--env-file credentials \
	-v $PWD/arma3:/arma3 \
	-v $PWD/profiles:/profiles \
	-v $PWD/my_mission/main.cfg:/server/main.cfg \
	-v $PWD/my_mission/basic.cfg:/server/basic.cfg \
	-p 2302:2302 \
	-p 2303:2303 \
	-p 2304:2304 \
	-p 2305:2305 \
	houki/arma3
```
