# Tower Defence Game

## How to play

The game starts with 25 Life points and $500. Press S to start a wave.

### Key Bindings

| Key | Action          |
| --- | --------------- |
| S   | Starts the wave |
| L   | Speeds up time  |
| K   | Slows down time |

### Defences - Buy Menu

| Defence                                                                                                      | Damage(HP) | Fire Rate(ps)                  | Effect Radius(units) | Cost($) |
| ------------------------------------------------------------------------------------------------------------ | ---------- | ------------------------------ | -------------------- | ------- |
| ![Tank](res/images/tank.png) ![TankProjectile](res/images/tank_projectile.png) Tank                          | 1          | 1                              | 100                  | $250    |
| ![SuperTank](res/images/supertank.png) ![SuperTankProjectile](res/images/supertank_projectile.png) SuperTank | 3          | 2                              | 150                  | $600    |
| ![AirSupport](res/images/airsupport.png) ![AirSupportExplosive](res/images/explosive.png) Air Support        | 500        | One Explosive Dropped Randomly | 200                  | $500    |

### Enemies

| Enemy                                                   | Health Points | Speed        | Kill Reward | Lives Penalty | Spawns            |
| ------------------------------------------------------- | ------------- | ------------ | ----------- | ------------- | ----------------- |
| Regular Slicer ![RegularSlicer](res/images/slicer.png)  | 1 HP          | 2 units/s    | $2          | 1 Life        | ~                 |
| Super Slicer ![SuperSlicer](res/images/superslicer.png) | 1 HP          | 1.5 units/s  | $15         | 2 Lives       | 2 Regular Slicers |
| Mega Slicer ![MegaSlicer](res/images/megaslicer.png)    | 2 HP          | 1.25 units/s | $10         | 4 Lives       | 2 Super Slicers   |
| Apex Slicer ![ApexSlicer](res/images/apexslicer.png)    | 25 HP         | 0.75 units/s | $150        | 16 Lives      | 4 Mega Slicers    |

## How to run

### Install Java

This Game uses Java 8 so it will need to be installed

### Install Maven - A Java Package Manager

Instructions to install maven can be found [here](https://maven.apache.org/install.html)

### install custom library

`mvn install:install-file -Dfile=lib/bagel-1.9.2.jar -DgroupId=unimelb -DartifaceId=bagel -Dversion=1.9.2 -Dpackaging=jar`

This is a wrapper around lwjgl - a lightweight java game library - found [here](https://gitlab.eng.unimelb.edu.au/emcmurtry/bagel-public)

### Install Dependencies and compile source code

| os                  | command                                    |
| ------------------- | ------------------------------------------ |
| macos intel         | `mvn install -P lwjgl-natives-macos`       |
| macos apple silicon | `mvn install -P lwjgl-natives-macos-arm64` |
| windows             | `mvn install -P lwjgl-natives-windows`     |
| linux               | `mvn install -P lwjgl-natives-linux`       |

### Run

`mvn exec:exec`
