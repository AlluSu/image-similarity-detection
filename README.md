# Digital Humanities Hackathon 2023, the Early Modern Group  

This repository contains code related to the course *Digital Humanities Hackathon* at University of Helsinki. For more information about the course and the projects can be found [here](https://www.helsinki.fi/en/digital-humanities/helsinki-digital-humanities-hackathon-2023-dhh23).  

## Instructions for running the code

### The script version *similarities.py*  
- Make sure you have Python with *pip* installed
- Clone the repository
- Run `pip install requirements.txt`
- Go to folder */code*  
- Usage: `similarities.py [-h] --inputpath INPUTPATH [--outputpath OUTPUTPATH] [--method METHOD] [--cutoff CUTOFF] [--amount AMOUNT]`

> Analyze images how similar they are, and write the results to a .csv file  
> options:  
>  -h, --help            show this help message and exit  
>  --inputpath INPUTPATH
>                        Relative path to the folder of the images  
>  --outputpath OUTPUTPATH
>                        Relative path to where the results will be stored  
>  --method METHOD       Use GPU or CPU for computing  
>  --cutoff CUTOFF       How similar images will be stored  
>  --amount AMOUNT       How many similar images will be stored  

For example:  
`python3 similarities.py --inputpath="../test-images/math-small" --outputpath="data/results" --method="cpu" --cutoff=0.93 --amount=5` 

### The jupyter notebook version

## Comparing two images for similarity  

During the DHH23 hackathon, I was assigned the task to analyse the images in the ECCO dataset for similar/identical images, as we were interested to see if some illustrations have provided inspiration for some other authors and have they been reused.  

### Image Hashing  

Principle of image hashing is relatively simple. Each image is hashed using some hashing algorithm, and these hashes are then compared. If the hashes differ a lot, we can reason that the images are not very similar. On the other hand, if the difference between the hashes is small, the images are similar.  

This technique is good for situations, were we would have a lot of very similar images or duplicates. In this case the term *very similar* means that there might be minor difference for example in lighting or in the quality. This technique won't recognize the differences so *broadly* compared to some other techniques, like *SIFT* or other machine learning/computer vision tricks.  

### Transfer learning with RESNET-18  




