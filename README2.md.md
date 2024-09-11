
# **CVAT Tool Enhancement: 3D to 2D Semantic Segmentation**

This enhancement to the CVAT (Computer Vision Annotation Tool) introduces a feature that automates the process of creating 2D semantic segmentation shapes from 3D data. The feature works on a **per-frame** basis, allowing users to generate and fine-tune 2D shapes corresponding to individual frames of the 3D data, simplifying the annotation process.

## **Table of Contents**

-   [Overview](#overview)
-   [Features](#features)
-   [Usage Instructions](#usage-instructions)
    -   [Step 1: Upload 3D Data & Calibration File](#step-1-upload-3d-data-and-calibration-file)
    -   [Step 2: Click the 3D to 2D Button](#step-2-click-the-3d-to-2d-button)
    -   [Step 3: Review 2D Shapes Per Frame](#step-3-review-2d-shapes-per-frame)
-   [Expected Output](#expected-output)
-   [Troubleshooting](#troubleshooting)
-   [Additional Notes](#additional-notes)

## **Overview**

This updated feature automates the creation of **2D semantic segmentation shapes** from 3D point cloud data on a **per-frame** basis. Users can extract outline points from the 3D shapes, project them onto 2D images, and create corresponding 2D polygons in CVAT for the selected frame. Each frame must be processed individually by clicking a button.

## **Features**

-   **Per-Frame Data Processing:** Users can generate 2D shapes for **individual frames** by selecting a frame and clicking a button.
-   **3D Shape Outline Extraction:** Automatically extracts outline points from 3D shapes for the current frame.
-   **2D Projection:** Projects 3D points onto 2D images while maintaining geometry, based on the calibration file.
-   **2D Segmentation Creation:** Creates polygonal shapes in CVAT for semantic segmentation corresponding to the 3D shapes in the selected frame.
-   **Duplication Prevention:** The system checks for duplicates using `clientID` to ensure no repeated shapes for the same object are created.

## **Usage Instructions**

### **Step 1: Upload 3D Data & Calibration File**

1.  **Prepare the 3D Data and Calibration File:**
    
    -   Upload the 3D point cloud or LiDAR data for your task, along with the **calibration file** for the camera or 3D sensor.
        
    -   The calibration file is essential for correctly projecting 3D points into the 2D space.
        
2.  **Verify Data:**
    
    -   Ensure that the 3D shapes and the calibration file are correctly loaded and displayed in CVAT.

### **Step 2: Click the 3D to 2D Button**

1.  **Ensure You Are in the 3D Task View:**
    
    -   This feature must be triggered when working within the 3D task.
2.  **Select the Desired Frame:**
    
    -   Navigate to the frame you want to project from the 3D data.
3.  **Click the "From 3D Segmentation" Button:**
    
    -   Click the **"3D to 2D Segmentation"** button in the CVAT interface. This will trigger the system to fetch the 3D data for the current frame, perform the projection, and generate the corresponding 2D segmentation shapes.

### **Step 3: Review 2D Shapes Per Frame**

1.  **Inspect the Created Shapes:**
    
    -   After clicking the button, review the 2D polygons that were generated from the 3D data for the selected frame.
2.  **Make Adjustments:**
    
    -   If necessary, adjust the shapes directly within CVAT’s interface for further fine-tuning.
3.  **Repeat for Other Frames:**
    
    -   Repeat this process for each frame individually by selecting the frame and pressing the button again.

## **Expected Output**

-   **Per-Frame 2D Segmentation:** After clicking the button on the current frame, 2D polygons are created based on the 3D shape outlines, projected correctly according to the calibration data.

## **Troubleshooting**

-   **Shapes Not Appearing:**
    -   **Solution:** Ensure you are in the correct frame, the 3D shapes are valid, and the calibration file is properly loaded.
-   **Incorrect Shape Projection:**
    -   **Solution:** Check the calibration file to ensure the correct data is used for projection.

## **Additional Notes**

-   **Per-Frame Processing:** Each frame must be processed individually by selecting the frame and clicking the button, allowing for granular control.
-   **Calibration Requirement:** The system depends on a valid calibration file to ensure accurate projection of 3D points into the 2D space.
-   **Reusability:** This process can be repeated for each frame and for different sequences of 3D data.
-   **Shape Editing:** After 2D segmentation shapes are created, they can be manually adjusted within CVAT’s interface, and the process can be retriggered if needed for changes in the 3D data
