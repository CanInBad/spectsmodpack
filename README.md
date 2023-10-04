# spectsmodpack
This is for both client and server

check [credits.md](credits.md) to view the credits

**it is still pretty good idea to read through the commit in each changes and debate them in the comment**

## Deploying on client
#### There are 2 ways of deploying on client
##### Zipped curseforge modpack

Requirements:
- [packwiz](https://github.com/packwiz/packwiz)

1. clone this repository
2. open terminal and cd yourself to cloned repository
3. `packwiz cf export`

it should create a zip in your cloned repo folder, then you can use the zip either drag and drop (multimc, prism launcher) or create new custom profile (curseforge launcher)

##### packwiz installer

Requirements:
- [packwiz](https://github.com/packwiz/packwiz)
- [packwiz-installer-bootstrapper](https://github.com/packwiz/packwiz-installer-bootstrap/releases)
- java/jdk/jre

1. download `packwiz-installer-bootstrapper` and put it where your .minecraft install should be
2. clone this repository
3. open terminal and cd yourself to cloned repository
4. `packwiz serve`
5. open another terminal and cd yourself to where you put `packwiz-installer-bootstrapper`
6. `java -jar packwiz-installer-bootstrap.jar -s client http://localhost:8080/pack.toml`
7. watch the terminal to see what mods are missing, then download said mods and put it in your .minecraft/mods

this should download all the mods and ready to launch

## Deploying on server

Requirements:
- [packwiz](https://github.com/packwiz/packwiz)
- [packwiz-installer-bootstrapper](https://github.com/packwiz/packwiz-installer-bootstrap/releases)
- java/jdk/jre

1. download `packwiz-installer-bootstrapper` and put it where your server
2. clone this repository
3. open terminal and cd yourself to cloned repository
4. `packwiz serve`
5. open another terminal and cd yourself to the server
6. `java -jar packwiz-installer-bootstrap.jar -g -s server http://localhost:8080/pack.toml`
7. watch the terminal to see what mods are missing, then download said mods and put it in your server's `mods` folder

this should download all the mods and ready to launch the server if you already installed forge server on the same folder

though if you want more info on packwiz, [see here](https://packwiz.infra.link/tutorials/creating/getting-started/)