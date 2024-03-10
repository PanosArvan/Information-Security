# Free Tickets

## [Video Killed the Text Star: OSINT Approach by Fran Gomez and Cesar Jimenez](https://www.youtube.com/watch?v=l822K95oZtE)

### Talks about open-source intelligence (OSINT) and Face Recognition.

*OSINT is the data collected from publicly available sources to be used in an intelligence context.*

Can be used in the context of:

- National Security
- Counterterrorism
- Cyber Tracking of persona non-grata
- Search missing people
- Identify people related to sexual violence crimes
- Identity theft
- Monitor competitors activities
- Gather information about a specific target (hacking)
- Marketing ROI (Sports, Youtube,...)

*Face recognition through video is one of the most advanced fields within machine learning in the past few years.*

1. HOG: Histogram of Oriented Gradients developed by Navneet Dalal and Bill Triggs in 2005.

Tries to detect when the dark spots in an image move and through gradients try to find patters.

Has difficulty when the person is not looking in the same direction as the original tracking image.

Is faster in processing than CNN.

Video form in real time.

2. CNN: Convolutional Neural Network

More precise in object recognition. 

Can be processed offline.


Those techniques can be used to identify all kinds of images, like building, cars, guns or even flags.

*Next step is do identify landmarks in the face.*

Face, nose, chin, eyebrows, nose bridge, nose tip, eyes, top lip, bottom lip and so on.

*Last step is facial recognition.*

Here we are checking for false positives (person detected but not in the image),
false negative (person not detected and in the image),
true positive (person detected and in the image) and
true negative (person not in the image but person detected).

To determine those, tolerance is used using Euclidean distance between vectors.

### Unknown Unknowns

Image processing/Topology

Tools used:

- OpenCV
- Apache Storm
- Dlib
- Face Recognition (python tool)

Process:

- Find internet videos
- Download with a downloader module
- Process videos
- Identify faces
- Use facial recognition to track known people or wanted people models
- Figure out what to do with unknown people or unknown relationships (categorize and group them)


Grouping:

Use Hash similarity or Perceptual Hash, pHash.
Those give a specific number that then can be traced back.
Problem is that it is influenced by background, brightness, face position and "noise" in general.

Other way is to use Clustering Mode k-Means.
It works properly only if you know how many people are in the video.

Last one is the Chinese Whispers. The one that works the best.
A node is assigned to a random class.
All the network nodes are selected 1by1 in a random order.
Every node moves to the class where the given node connects with the most links.
In case of equality it is randomly chosen.
Step two repeats itself until the process converges.
In the end the emerging classes represent the clusters of the network.


*Three dimenstional facial recognition.*

Requires spatial cameras that use a series of sensors.

Apple's FaceID and Intel's RealSense.
