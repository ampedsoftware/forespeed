# ForeSpeed Dataset

ForeSpeed includes 322 vehicle passing under CCTV cameras with various settings.

Since the dataset is designed for forensic assessment, we take care of preserving the original video information that is relevant for the task, such as the presentation timestamps (PTS) of variable frame rate videos when available.

The dataset is detailed in the paper

_ForeSpeed: A real-world video dataset of CCTV cameras with different settings for vehicle speed estimation_

Authors: _Massimo Iuliani, Blake Sawyer, Marco Fontani, David Spreadborough, and Martino Jerian_ from _Amped Software_ and _Amped Software USA_

## Dataset Structure
The dataset is structured as follows:

- six folders, each containing the data acquired by a CCTV camera model (e.g., _Eufy_);
- each folder may contain multiple sub-folders if more than one camera and storing format is available (e.g., Lorex/cam1/main/avi). These folders may include different CCTV cameras plugged into the same DVR, multiple quality streams available by the DVR, and multiple compression settings.
- each sub-folder contains the passing (see the paper) under two different perspective conditions.

When possible, the video containing the car passing is stored with the name `T < x > P < y >-<camera name>-<details>`, where `T1` and `T2` stand for low and strong perspective
respectively and P identifies the passing (e.g., `T1P5-Ring-6996443541347278144` stands for the passing 5 with a low perspective in the camera `Ring`).

Since each camera uses a different acquisition protocol, some exceptions occurred:
- Anran acquisition is split in four videos of 15 minutes each;
- in some cameras the video acquisition is automatically split. When the split occurs
during the vehicle passing, two videos of the same passing are included in the dataset (e.g., Lorex/cam1/main/avi/T1P4);

The number of the test and the car passing is displayed on a board shown by the authors directly on screen before the action takes place.

In the paper appendix we report the ground truth speed for each pass in each test.