
# CVAT Tool Enhancement: Bounding Box Creation and Grouping for Polygons

This enhancement to the CVAT (Computer Vision Annotation Tool) introduces a feature that automatically creates and groups bounding boxes for each polygon in a frame, streamlining the annotation process.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Usage Instructions](#usage-instructions)
  - [Step 1: Draw Polygons](#step-1-draw-polygons)
  - [Step 2: Create Bounding Boxes for All Polygons](#step-2-create-bounding-boxes-for-all-polygons)
  - [Step 3: Group Polygons with Bounding Boxes](#step-3-group-polygons-with-bounding-boxes)
- [Expected Output](#expected-output)
- [Troubleshooting](#troubleshooting)
- [Additional Notes](#additional-notes)

## Overview

This feature allows users to automatically create bounding boxes for all polygons in a frame by clicking the "Group" button. Upon a second click, each polygon is grouped with its corresponding bounding box, enhancing annotation management and efficiency.

## Features

- **Automatic Bounding Box Creation:** Generates bounding boxes for all polygons in a frame with a single click.
- **Grouping Functionality:** Groups each polygon with its corresponding bounding box upon a second click.
- **Enhanced Annotation Management:** Simplifies the handling and editing of annotations.

## Usage Instructions

### Step 1: Draw Polygons

1. **Open a Project:**
   - Launch CVAT and open the project you wish to annotate.
   
2. **Draw Polygons:**
   - Use the polygon tool to draw the required polygons on your images .

![Drawing Polygons](https://github.com/SalmaElsaid/image-of-cvat/blob/main/draw_polygon.png)

### Step 2: Create Bounding Boxes for All Polygons

1. **Click the "Group" Button:**
   - Locate and click the **"Group"** button in the CVAT interface.
   
    ![group button ](https://github.com/SalmaElsaid/image-of-cvat/blob/main/group_button.png)
   
2. **Automatic Bounding Boxes:**
   - Bounding boxes will be generated for all existing polygons in the current frame.

   ![Bounding Boxes Created](https://github.com/SalmaElsaid/image-of-cvat/blob/main/bounding_box.png)

### Step 3: Group Polygons with Bounding Boxes

1. **Click the "Group" Button Again:**
   - Click the **"Group"** button a second time.
   
2. **Grouped Annotations:**
   - Each polygon will be grouped with its corresponding bounding box, allowing for unified manipulation.

   ![Grouped Annotations](https://github.com/SalmaElsaid/image-of-cvat/blob/main/grouping_shapes.png)

## Expected Output

- **First Click on "Group":** Bounding boxes are created for all polygons in the frame.
- **Second Click on "Group":** Each polygon is grouped with its corresponding bounding box, facilitating easier management and editing.

## Troubleshooting

- **Bounding Boxes Not Created:**
  - **Solution:** Ensure that all polygons are properly drawn. Check for any console errors in CVAT.
  
- **Grouping Fails:**
  - **Solution:** Make sure to click the "Group" button a second time. Verify that both polygons and bounding boxes are present.

## Additional Notes

- **Reusability:** The grouping action can be repeated as needed by clicking the "Group" button.
- **Compatibility:** Works with all polygon shapes and sizes.
- **Editing:** all shapes polygon or rectangles can be edited.




