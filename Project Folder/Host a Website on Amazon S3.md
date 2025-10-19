<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Gospel Opara  
**Email:** oparagospel001@gmail.com

---

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use S3 to host a static website. I'm doing this project to learn about AWS and cloud services and how they can be use to store object and host website.

### Tools and concepts

Services I used were Amazon S3 Key concepts I learnt include bucket policy, uploading static html files, bucket input URL and ACL and how they control access to our bucket.

### Project reflection

This project took me approximately 50 mins. The most challenging part was resoling the 403 forbiden error. It was most rewarding to see our web page go live to the world.

---

## How I Set Up an S3 Bucket

Creating an S3 bucket took me kess than 5 min,learnt a few new concept like ACL and bucket policy.It will take fewer mins as it progresses.

The Region I picked for my S3 bucket was Paris because its the region closest to me which lowers time to retrieve  project, reduce lantecy and cost

S3 bucket names are globally unique! This means no two AWS bucket in the world can have the same name regardless of the region and time

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### index.html and image assets

I uploaded two files to my S3 bucket - they were html index file which determines the structure and Network everybody love files which fills the website with images and structures.

Both files are necessary for this project as html index is used to create and design web pages which determines the structure but the structure alone does not illlustrate the content of the website. The images needs to be supplied separately.

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

Website hosting means putting the website site in a web server which will turn our website page into a website, making our website public on the internet.

To enable website hosting with my S3 bucket, I configured my S3 bucket for ststic hosting

An ACL is an access control list is a way a configure access control list in a bucket. This compared to bucket policy which is mostly used today

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

Once static website is enabled, S3 produces a bucket endpoint URL, which is     http://network-website-project-opara.s3-website.eu-west-3.amazonaws.com/

When I first visited the bucket endpoint URL, I saw... The reason for this error was a 403 forbidded error the reason for the error was the website file itself is still private.
It has to be public to see the content of the website 

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

To resolve this 403 Forbidden error, I updated the access setting of the files inside our bucket using ACL I made the file public.

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

An alternative to ACLs are bucket policies, which are rules that determine who is allowed or who is not allowed. The benefit of using bucket policies is has even greater control of who has access of the actions that people are allowed to do or not  while ACLs are useful for are useful for control public access inside the bucket.

My bucket policy deenies everyone from deleting my index.html file. I tested this by deleting the index.html file and saw the permisiion denial error, which means the bucket policy worked.

![Image](http://learn.nextwork.org/cheerful_chartreuse_swift_ginger/uploads/aws-host-a-website-on-s3_sm2sm2sm)

---

---
