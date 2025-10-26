Data: Drone swarm strategy for the detection and tracking of occluded targets in complex environments
====================================================================

**Abstract:**
Drone swarms can achieve tasks via collaboration that are impossible for single drones alone. Synthetic aperture (SA) sensing is a signal processing technique that takes measurements from limited size sensors and computationally combines the data to mimic sensor apertures of much greater widths. Here we use SA sensing and propose an adaptive real-time particle swarm optimization (PSO) strategy for autonomous drone swarms to detect and track occluded targets in densely forested areas. Simulation results show that our approach achieved a maximum target visibility of 72% within 14 seconds. In comparison, blind sampling strategies resulted in only 51% visibility after 75 seconds and 19% visibility in 3 seconds for sequential brute force sampling and parallel sampling respectively. Our approach provides fast and reliable detection of occluded targets, and demonstrates the feasibility and efficiency of using swarm drones for search and rescue in areas that are not easily accessed by humans, such as forests and disaster sites.

**Authors:** **Rakesh John Amala Arokia Nathan**, Indrajit Kurmi, Oliver Bimber

## Data

The folder `data` contains the following datasets: 

* Sequentially_sampling_single_camera_drone
* Parallelly_sampling_camera_array
* Swarm_of_three_camera_drones_S3_result1
* Swarm_of_three_camera_drones_S3_result2
* Swarm_of_three_camera_drones_S3_result3
* Swarm_of_five_camera_drones_S3_result1
* Swarm_of_five_camera_drones_S3_result2
* Swarm_of_five_camera_drones_S3_result3
* Swarm_of_ten_camera_drones_density_300_S3_result1
* Swarm_of_ten_camera_drones_density_300_S3_result2
* Swarm_of_ten_camera_drones_density_300_S3_result3
* Swarm_of_ten_camera_drones_density_400_S3_result1
* Swarm_of_ten_camera_drones_density_400_S3_result2
* Swarm_of_ten_camera_drones_density_400_S3_result3
* Swarm_of_ten_camera_drones_density_500_S3_result1
* Swarm_of_ten_camera_drones_density_500_S3_result2
* Swarm_of_ten_camera_drones_density_500_S3_result3
* Motion_tracking_linearpath
* Motion_tracking_circularpath
* Failure_case1_too_fast_target
* Failure_case2_locally_too_dense_occlusion


Each dataset contain the following 12 subfolders:

* debug
* masked_integral 
* masked_integral(with_history)
* objective_metric_plot
* Result
* RGB(single_images)
* RGB_integral
* RGB_integral(with_history)
* stage_images
* Thermal(single_images)
* Thermal_integral
* Thermal_integral(with_history)


The debug folder contains metric_area.json (objective metric for each waypoint), time_taken.json(time taken in seconds for all drones to reach a waypoint) and Info.txt containing information about the dronepositions,velocity vector, leader etc. for debugging purpose.The masked_integral folder contains the integrated binarized results of the images captured at the given waypoint after anomaly score thresholding while masked_integral(with_history) folder contains integrated binarized results of the images captured at the given waypoint along with those history images that improves our objective. The objective_metric_plot folder contains plots (Time(seconds) vs Metric) computed at each waypoint. Result folder contains the final 2D results of the experiments for each waypoint. The RGB(single_images) and the Thermal(single_images) folder contains sub-folders that corresponds to each drone with RGB and thermal images captured at each waypoint respectively using the AOS-simulator. The stage_images folder contains top-down images of the simulation environment captured at each waypoint. The RGB_integral and Thermal_integral folders contain integrated RGB and thermal images for each given waypoint respectively with the RGB_integral(with_history) and Thermal_integral(with_history) folders containing integrated RGB and Thermal images captured at each given waypoint along with those history images that improves our metric.



Further details can be found in the main article and supplementary material of our publication: [Communications engineering](https://www.nature.com/articles/s44172-023-00104-0).

## Citation

If you use this dataset or code, please cite:
```bibtex
@article{amala2023drone,
  title={Drone swarm strategy for the detection and tracking of occluded targets in complex environments},
  author={Amala Arokia Nathan, Rakesh John and Kurmi, Indrajit and Bimber, Oliver},
  journal={Communications Engineering},
  volume={2},
  number={1},
  pages={55},
  year={2023},
  publisher={Nature Publishing Group UK London}
}