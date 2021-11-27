Welcome to the _Github_ organization of

# Solar Swarm Clean

### [Prerequisite](https://github.com/Solar-Clean/.github#prerequisite)

### Installation

#### 1)

Go to the directory where you want the projekt to be located. Then run

```bash
mkdir -p solar-swarm-ws/src && cd solar-swarm-ws/src
```

This will create a new directory `solar-swarm-ws` and a subdirectory `src` inside the current folder. You can choose a different name for the top level directory ,
but naming the subdirectory `src` is mandatory for _ROS_.

#### 2)

Now, as you should be in `src` you can clone the _solar-swarm-utils_ repository. Therefore, run:

```bash
git clone git@github.com:Solar-Clean/solar-swarm-utils.git
```

This requires you to have git installed and ssh set up. If you don't have ssh set up you can use the https link instaed, which you can find in the repository.

#### 3)

Use `cd solar-swarm-utils` to go into the folder with the repository created in the previous step.

You can now start the actual installation. Run:

```bash
chmod +x install.sh
```

to make the installation script executable. After that, you should execute it by running:

```bash
./install.sh *args
```

where args is either _drone_, _roboter_ or both. 

The installation script will then install `ros-noetic-desktop-full` and a lot of required dependencies. Additionally poetry, a python package manager, is installed, which will manage virtual python environments. 
During the installation multiple aliases are added to your shell aliases file:
- `make_drone` automatically calls catkin_make in the workspace directory
- `workon_solarswarm` which will direct you inside the workspace and start the poetry shell
- `solarswarm` sources the ros setup script and adds the source directory to your ROS_PACKAGE_PATH

### Workflow

When starting to work on the projekt you should call `workon_solarswarm` and `solarswarm` in order.

After you have changed any files you should call `make_drone` to compile the whole project.

### Usage

#### Drone


__TODO__
