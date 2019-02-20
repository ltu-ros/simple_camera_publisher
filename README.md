# Simple Camera Publisher

This package publishes a hardware camera as an OpenCV image. 

Publish your machine's default camera:

```
roslaunch simple_camera_publisher example.launch
```

## How to use

```xml
<launch>
    <!-- The name of the camera -->
    <group ns="my_camera">

        <!-- launch the node -->
        <node name="cam_pub" pkg="simple_camera_publisher" type="cam_pub" respawn="true" respawn_delay="10" output="screen">
          
            <!-- Use a specific camera path -->
            <!--<param name="source" type="string" value="/dev/v4l/by-id/my_camera_id" /> -->

            <!-- Flip the image before publishing -->
            <param name="hflip" type="bool" value="false" />

            <!-- Show output in CV window -->
            <param name="show_output" type="bool" value="true" />
        </node>

    </group>
</launch>

```
