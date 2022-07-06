# Mid-term project:3D object detection
## project overview

 In this project, a deep-learning approach is used to detect vehicles in LiDAR data based on a birds-eye view perspective of the 3D point-cloud. 
 Also, a series of performance measures is used to evaluate the performance of the detection approach.

## Section 1 :Compute Lidar Point-Cloud from Range Image
- **Visualize range image channels**

  In the Waymo Open dataset, lidar data is stored as a range image. we need to extract the data from `range` and `intensity` channels within range image.
  Then convert the floating-point data to an 8-bit integer value.
  
    ***Image display***
    
    ![s1_ex1](./img/s1_ex1.png)
   
- **Visualize lidar point-cloud**

  This task is to use the Open3D library to display the lidar point-cloud in a 3d viewer.
  
    ***varying degrees of visibility***
    
    | ![s1_ex2-1](./img/s1_ex2-1.png) | ![s1_ex2-2](./img/s1_ex2-5.png) |
    |     :---:     |     :---:      |
    | ![s1_ex2-3](./img/s1_ex2-2.png) | ![s1_ex2-4](./img/s1_ex2-4.png) |
    | ![s1_ex2-5](./img/s1_ex2-3.png) | ![s1_ex2-4](./img/s1_ex2-6.png) |

## Section 2 : Create Birds-Eye View from Lidar PCL
- **Convert sensor coordinates to BEV-map coordinates**

  ***Image display***
  
  ![s2_ex1](./img/s2_ex1.png)

- **Compute intensity layer of the BEV map**

  ***Image display***
  
  ![s2_ex2](./img/s2_ex2.png)
  
- **Compute height layer of the BEV map**

  ***Image display***
  
  ![s2_ex3](./img/s2_ex3.png)

## Section 3 : Model-based Object Detection in BEV Image
- **Add a second model from a GitHub repo**

  This task is to integrate `fpn_resnet` into an existing framework

  ***Result***
  
  ![s3_ex1](./img/s3_ex1.png)

- **Extract 3D bounding boxes from model response**

  ***Image display***
  
  ![s3_ex2](./img/s3_ex2.png)
  
## Section 4 : Performance Evaluation for Object Detection
- **Compute intersection-over-union between labels and detections**
- **Compute false-negatives and false-positives**
- **Compute precision and recall**

***Image display***

   | `configs_det.use_labels_as_objects = False` | `configs_det.use_labels_as_objects = True` |
   |     :---:     |     :---:      |
   | ![s4_ex3-2](./img/s4_ex3-2.png) | ![s4_ex3-4](./img/s4_ex3-4.png) |
   | **precision = 0.95409, recall = 0.95098** | **precision = 1.0, recall = 1.0** |




