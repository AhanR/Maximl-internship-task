# Maximl-internship-task

## Problem 1:
_To find all the anagrams and group them_
### Approach:
- I first tried the brute force algorithm with about O(n^2) complexity which felt like it could use some adjustments
- Next, I tried hashing the words to make the anagrams easier to compare, this method worked
- Converted the frequency list to a string and used that to hash the words
- This solution works in about O(n) time considering that the words are hashed in almost constant time due to their small size
### Challenges:
- The time complexity of the first solution was not good enough
- The hashing function to be used was slightly confusing at first

## Problem 2:
_To manipulate videos using open cv_
### Approach:
- First, I looked up any pre existing tutorials on the topic to realise none exist in the form needed
- Then I tried to understand how to read, write and manipulate video streams in cv2
- Then I sat down and brainstormed how to sample the frames to maintain the time of the video (screenshot available below)
- After some tinkering, I was able to implement the sampling technique (for x frames in the source whose duration exceeds the duration of the corresponding frame in the target, sample the topmost frame from the source)
- Adding text and converting to greyscale were relatively simple tasks
### Challenges:
- The first and biggest challenge for me was to figure out the sampling technique to maintain the time of the video
- The second challenge I ran into was the target video file being empty, the image when converted to Greyscale no longer had BGR values, insted it had a single value, so I had to convert the image back into BGR format for the frame to be written to target file
- The last challenge was verifying the results which I was able to solve pretty quickly

Screenshot of the thought process that I went through for the second problem statement
![working](https://github.com/AhanR/Maximl-internship-task/assets/64554828/fc3c39c1-341a-48a5-8f76-4a8347df8680)

# Problem 3:
_To extract text from image and draw bounding box around it_
### Approach:
- First, install pyTesseract
- Then I experimented with different modes and different configurations to finally figure out that there are 2 modes which can be used togethter to get maximum text
- Run the OCR module on the image twice to get both vertical and horizontal text
- Plot the boxes on the image and the text. I also added in a confidence percentage to be able to better understand what is going on under the hood and how to optimise it
- Plot the image to the output in colab
- I additionally went ahead and configured a few more languages to see if the kannada text could be better read but that did not yield any result
### Challenges:
- Installation of pyTesseract took me some time, especially figuring out why it was not working but thankfully, there were a few helpful posts on stack overflow
- With any given mode only about 50% of the text was read and had terrible accuracy, so I had to combine 2 modes and filter by the confidence level to get better results

The two selected modes, mode 5 for vertical text:
![image](https://github.com/AhanR/Maximl-internship-task/assets/64554828/dcb39867-6037-4ac3-b16a-f6168168cd0f)
mode 11 for horizontal sparse text:
![image](https://github.com/AhanR/Maximl-internship-task/assets/64554828/a5e40736-1ff2-4f7d-ad2a-fa7a75f909ba)

# Imporovements I'd like to make:
- For the second problem statement, I'd like to interpolate the images in such a way that even the skipped frames can add some presence to the target frame by means of projection to the un skipped frame
- For the third problem, I'd like to experiment a bit more with the OCR configurations, I have gone over a lot of the suggested parameters but it still fails on some images and I'd like to look into other parameters to try and improve on that

# Why me?
- I was able to complete this assignment in under 7 hours, this is the kind of  energy that I bring to the table
- I am a frequent contributor on GitHub and have many contributions to my own repositories, others repositories and even some open source projects
- I like learning new tech and almost always like to experiment with new languages, libraries and frameworks
- I want to try and apply some of my skills in real world applications and see where I stand
- I really like the company ethos and I think I will be able to blend well

Either ways, thanks for the opportunity.
