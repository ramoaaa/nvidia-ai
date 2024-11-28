# Oxygen fire detection model using YOLOv5

# **Project Overview**

**Introduction to background information**

Outdoor fire hydrants are essential safety equipment for initial fire suppression and are strategically placed outside buildings and in public spaces. However, if the exact location of a fire hydrant is unclear or if obstacles obstruct access, it can reduce accessibility during emergencies, leading to delays in disaster response. These challenges highlight the need for technologies to search for and identify fire hydrants, suggesting the potential application of artificial intelligence (AI)-based object detection technologies.

 General Description of the Current Project

The primary goal of this project is to develop a robotic system capable of quickly detecting outdoor fire hydrants and efficiently suppressing fires in the event of an outbreak outside a building. This system utilizes a camera and an AI-based object detection model, YOLOv5, to automatically identify fire hydrants in the surrounding environment. The robot is designed to navigate to the detected hydrant's location and carry out fire suppression tasks. Such a system aims to reduce response times during fire emergencies and minimize potential fire damage.

 **Proposed Idea for Enhancements to the Project**

1.

**Real-Time Detection and Rapid Response**

The outdoor fire hydrant detection system leverages the high computational efficiency of YOLOv5 to identify fire hydrants in real-time. This capability allows for quick identification of hydrant locations, enabling immediate responses during emergencies.

1. 

**High Adaptability to Diverse Environments**

Outdoor fire hydrants are often situated in environments with varying lighting, weather conditions, and obstacles. This system is designed to minimize environmental limitations by utilizing data augmentation and model tuning, ensuring high detection accuracy even in challenging conditions.

1. 

**Enhancement of Public Safety Networks**

The rapid detection of outdoor fire hydrants reduces fire response times, thereby contributing to the prevention of property damage and loss of life. Additionally, it promotes the digitization of public infrastructure, strengthening safety networks and enhancing overall public safety.

 **Value and Significance of this Project**

This project aims to support initial fire response to prevent the spread of fires, promote the digitization of public infrastructure as part of smart city development, and enhance reliability in disaster scenarios through rapid and accurate responses. Additionally, it effectively contributes to reducing the social and economic costs associated with fire incidents.

**Current Limitations**

- **Data Collection and Labeling**: Acquiring outdoor fire hydrant data captured in various environments requires significant time and resources.
- **Performance Degradation Due to External Factors**: Variations in lighting, obstacles, and weather conditions can impact detection accuracy.

**Literature Review**

Research on outdoor fire hydrant detection is still in its early stages both domestically and internationally. This project holds a pioneering significance as it explores the practical applicability of YOLOv5 for this purpose.

**Project Progress**

The recorded videos were converted into frame-by-frame images, and annotations were created using **DarkLabel**, a well-known Video/Image Labeling and Annotation Tool.

1. **Install DarkLabel.exe**
    
    Install the DarkLabel executable file.
    
2. **Edit the darklabel.yml file**
    
    Modify the `darklabel.yml` file as follows:
    
    - **Step 2-1:** Add `fireplug_class: ["fireplug"]` to **Predefined Classes Sets**.
    - **Step 2-2:** Add `format9` to **User-defined GT Formats**.
3. **Run the DarkLabel program**
    
    Launch the DarkLabel program.
    
4. **Import video for annotation**
    
    Open the video to be used for training through the **Open Video** option.
    
![스크린샷 2024-11-28 225153](https://github.com/user-attachments/assets/ff3aff65-939b-46f5-bd8f-58c00f5f7de7)

### **5. Controls for Object Annotation**

- **5-1.** `Shift + Right-click`: Delete a bounding box
- **5-2.** `Shift + Left-click`: Move a bounding box
- **5-3.** `Space bar`: Move to the next frame

After labeling all frames, download the respective data files.

### **6. Saving Data Files**

- **6-1.** `As Images..`: Save each frame as an image
- **6-2.** `GT Save As..`: Save the label values for each frame
![스크린샷 2024-11-28 225615](https://github.com/user-attachments/assets/6aa9a875-123f-49c4-b216-e2d3442d9267)
**Results**
![스크린샷 2024-11-28 225643](https://github.com/user-attachments/assets/e97d0030-1813-4d41-a89f-e6e4c3923dc9)

- **TensorBoard**
![스크린샷 2024-11-28 225744](https://github.com/user-attachments/assets/fa7d66a4-f911-4e5d-b55e-3e7a7cdbce33)

• **Confusion Matrix**
![스크린샷 2024-11-28 225841](https://github.com/user-attachments/assets/00ebb1b2-dc24-4c9b-bb12-b330bc0cc1ac)

- **F1-Curve**
![스크린샷 2024-11-28 225902](https://github.com/user-attachments/assets/ded48972-e8ef-4805-b406-fe267bec85cc)

- **labels_correlogram**
![스크린샷 2024-11-28 225930](https://github.com/user-attachments/assets/76b1489a-06a8-4c11-8dcc-f94735e55b96)

- **labels**
![스크린샷 2024-11-28 230004](https://github.com/user-attachments/assets/ddf287f9-e302-4e63-a729-ea6ec15a617b)

- **P-Curve**
![스크린샷 2024-11-28 230031](https://github.com/user-attachments/assets/ac94df98-a426-4956-82a8-6e9021925d26)

• **Result**
![스크린샷 2024-11-28 230112](https://github.com/user-attachments/assets/33503660-9dd6-4001-827c-adf93838d918)

- **Train batch**
![스크린샷 2024-11-28 230150](https://github.com/user-attachments/assets/62ca3adf-abcf-4b3f-b376-5e3126673e93)
![스크린샷 2024-11-28 230158](https://github.com/user-attachments/assets/68b6fdcd-74be-4f73-9e19-2473074322e9)
![스크린샷 2024-11-28 230215](https://github.com/user-attachments/assets/86366f90-ce03-4b41-91bf-d1c91bf38552)

**Detect**
![스크린샷 2024-11-28 230417](https://github.com/user-attachments/assets/6a34d5f4-1368-494d-8a96-5c290b19116f)

### **Video Acquisition**

Outdoor fire hydrants were captured in various controlled environments to build a robust dataset for training and validation. The recorded scenarios include:

- Fire hydrants located outside buildings
- Fire hydrants observed from various angles and distances

**Training Video**

https://drive.google.com/drive/folders/1QqKo7ABrH2F_IHHPl1-26uVHyUGQlKC7?usp=drive_link

**Validation Video**

https://drive.google.com/drive/folders/1Hg8wbtq5T-OmuUFmZFCHV5m1F-J7GCZb?usp=drive_link

**Jetson Nano**
https://learn.nvidia.com/certificates?id=17jjKXoaQumrqAILF9Wyvw




