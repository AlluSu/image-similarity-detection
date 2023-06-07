# Digital Humanities Hackathon 2023, the Early Modern Group  

This repository contains code related to the course *Digital Humanities Hackathon* at University of Helsinki. For more information about the course and the projects can be found [here](https://www.helsinki.fi/en/digital-humanities/helsinki-digital-humanities-hackathon-2023-dhh23).  

## Instructions for running the code

### The script version *similarities.py*  
- Make sure you have Python with *pip* installed
- Clone the repository
- Run `pip install requirements.txt`
- Go to folder */code*  
- Usage:  
`similarities.py [-h] --inputpath INPUTPATH [--outputpath OUTPUTPATH] [--method METHOD] [--cutoff CUTOFF] [--amount AMOUNT]`

> Analyze images how similar they are, and write the results to a .csv file  
> options:  
>  -h, --help            show this help message and exit  
>  --inputpath INPUTPATH
>                        Relative path in quotes ("") to the folder of the images, requires  
>  --outputpath OUTPUTPATH
>                        Relative path in quotes ("") to where the results will be stored, default is the same directory  
>  --method METHOD       "GPU" or "CPU" for computing, default is "CPU"  
>  --cutoff CUTOFF       How similar images will be stored, between 0 to 1, where larger number indicates more similar images. Default is 0.9  
>  --amount AMOUNT       How many similar images will be stored, default is 5  

For example:  
`python3 similarities.py --inputpath="../test-images/math-small" --outputpath="data/results" --method="cpu" --cutoff=0.93 --amount=5` 

### The jupyter notebook version
- Make sure you have Python with *pip* installed
- Clone the repository
- Run `pip install requirements.txt`
- Go to folder */code*
- Run `jupyter-notebook` and the Jupyter environment should open automatically in your local browser  

## Image Similarity Detection techniques  

You can read more about the research and techniques related to detecting similar images from this [report](/code/DHH23-report.pdf)  

