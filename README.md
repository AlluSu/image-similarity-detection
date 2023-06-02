# Digital Humanities Hackathon 2023, the Early Modern Group  

## Comparing two images for similarity  

This is a repository for a PoC of a program for comparing two images using image hashing.  

During the DHH23 hackathon, I was assigned the task to analyse the images in the ECCO dataset for similar/identical images, as we were interested to see if some illustrations have provided inspiration for some other authors and have they been reused.  

After doing some research, it seemed that there were few available techniques to do this, which the first one I tried being Image Hashing.  

### Image Hashing  

Principle of image hashing is relatively simple. Each image is hashed using some hashing algorithm, and these hashes are then compared. If the hashes differ a lot, we can reason that the images are not very similar. On the other hand, if the difference between the hashes is small, the images are similar.  

This technique is good for situations, were we would have a lot of very similar images or duplicates. In this case the term *very similar* means that there might be minor difference for example in lighting or in the quality. This technique won't recognize the differences so *broadly* compared to some other techniques, like *SIFT* or other machine learning/computer vision tricks.  

### Transfer learning with RESNET-18  




