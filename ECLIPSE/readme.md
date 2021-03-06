
*Please do not download nor redistibute any parts of this ECLIPSE copy.*

## Requirements

The copy is owned by Dr. Don Sin. To obtain read-access to this copy, you must obtain his permission and become a member of ```acl-ubc-med-img``` through Compute Canada.

## Steps to access the data

1. Become a member of Group ```acl-ubc-med-img```
2. SSH to Graham via this command: 
    ```ssh username@graham.computecanada.ca```
    
2. Navigate to the folder; i.e. 
    ```
    cd /project/def-donsin/shared-folder/ECLIPSE/
    ```

## Folder structure

- Command below will show you a *list* of folders named by subject (i.e. one folder for each subject, with all timepoints in each subfolder). 

  ```
  ls /project/def-donsin/shared-folder/ECLIPSE/  
  ls -lstr /project/def-donsin/shared-folder/ECLIPSE/     # list and to see the access permissions as well as other info
  ```

- To view the contents of each subfolder, you may use the ```cd``` command to *change* into a *directory*, and the ```ls``` command to list, e.g.:

  ```
  cd /project/def-donsin/shared-folder/ECLIPSE/026658003987/
  ls -d */
  ```

## Brief summary about the filenames

- Subject ID: last 4 digits 
- Bone vs. STD (standard) kernel
- L1: first timepoint, L2: second timepont, etc.

e.g. 

```026658003987_INSP_STD_L2_ECLIPSE```

```026658003987_INSP_BONE_L3_ECLIPSE```



