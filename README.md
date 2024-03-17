# lilypad_pointcloud_module
repository for adding  job module templates to run  point cloud preprocessing jobs on our instance, for demo checkout [here](https://docs.lilypad.tech/lilypad/lilypad-aurora-reference/build-a-job-module). 

Each of the branch in the given repository consist of the various templates for running the job modules from one of the docker images from the [devextralabs]([text](https://hub.docker.com/repositories/devextralabs) registry.



## Running command:


1. Followup the setup for the lilypad and bacalhau instances from [here]()


2. pass the variables here: 
```bash

lilypad run "https://github.dev/The-Extra-Project/lilypad_pointcloud_module:cropping" -i  Coordinates="twoD"  Points=()CRS ....

```

here:
    - Coordinates are used in order to select the category of points that you want to pass for the cropping operations.
        - if its threeD:  `Points=(Xmax,Xmin, Ymax, Ymin) CRS="WGS84"` are the boundation points of the given polygon area.
        - if itx twoD:  `Points=(X,Y) radius=10, CRS=WGS84` are the boundation points of the area covered from the given center across the area covered by the radius.
    