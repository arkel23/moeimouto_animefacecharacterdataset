Scripts to create a data dictionary from an ImageNet-style folder. 
Default behavior is to check all the folders for jpg, jpeg and png files.
Then, the files are checked to verify they're RGB images (excludes RGBA and other image modes).
It then saves those into a dataframe with the class ID and the relative path to the image.
The absolute path is the path to the folder in which it's looking for + the relative path.
The class names are inferred from the folders in which the images are contained.
These class names along with the respective class IDs are also saved to a {datasetname}_classid_classname.csv

Also includes script to split the resulting data dictionary into train and test splits.
Default split percentages are 80 and 20%, respectively. 

ImageNet-style folder:
```
ImageNet/class1/img1
ImageNet/class1/img2
...
ImageNet/classX/imgX
```

Usage:
```
python make_data_dic_imagenetstyle.py . # run in the root folder
data_split.py {dataset_name}.csv # dataset_name = root folder name
```
