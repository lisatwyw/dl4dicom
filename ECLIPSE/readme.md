
*Please do not download nor redistibute any parts of this ECLIPSE copy.*

## Requirements

This copy of the ECLIPSE is owned by Dr. Don Sin. Accordingly, to access this copy, you must obtain permission and become a user of Group ```acl-ubc-med-img```.

## Steps to access the data

1. Become user of  Group ```acl-ubc-med-img```
2. SSH to graham via this command: 
    ```ssh username@graham.computecanada.ca```
    
2. Navigate to the folder; i.e. 
    ```
    $ lstr /project/def-donsin/shared-folder/ECLIPSE/
    ```

## Folder structure

- Command below will show you a *list* of folders named by subject (i.e. one folder for each subject, with all timepoints in each subfolder). 

  ```
  $ ls /project/def-donsin/shared-folder/ECLIPSE/  
  $ lstr /project/def-donsin/shared-folder/ECLIPSE/     # Or, to see the access permissions as well
  ```

- To view the contents of each subfolder, you may use the ```cd``` command to *change* into a *directory*, and the ```ls``` command to list, e.g.:

  ```
  cd /project/def-donsin/shared-folder/ECLIPSE/026658003987/
  ls -d */
  ```

## Brief summary about the filenames

- Study ID: last 4 digits 
- Bone vs. standard kernel
- L1: first timepoint, L2: second timepont, etc.

e.g. ```026658003987_INSP_STD_L2_ECLIPSE```, ```026658003987_INSP_BONE_L3_ECLIPSE```


