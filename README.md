# IVI Media Service and Audio HAL Message Flow Simulation

## Module 6 – IVI In-Vehicle Infotainment Systems

### Project Type

Simulation of message flow between the Media Service and Audio HAL in an In-Vehicle Infotainment (IVI) system.

---

## 1. Project Overview

This project demonstrates how a user's media-related action in an In-Vehicle Infotainment system propagates through different software and hardware abstraction layers.

The simulation models the communication flow between:

```text
User
  ?
IVI User Interface
  ?
Media Service
  ?
Audio Framework
  ?
Audio HAL
  ?
Audio Driver
  ?
Vehicle Speakers
```

The project uses Python to simulate system events and generate Android-style log messages representing the communication between the different components.

---

## 2. Objective

The main objectives of this project are:

* To understand the basic architecture of an IVI media system.
* To demonstrate message propagation from the user interface to the audio output.
* To simulate communication between the Media Service and Audio HAL.
* To generate system logs for different media operations.
* To visualize the IVI message-flow architecture.
* To analyze the number and type of messages processed by each component.

---

## 3. Simulated Operations

The project simulates the following user actions:

* Play
* Pause
* Resume
* Volume Change
* Stop

For each operation, the system generates a sequence of messages showing how the command moves through the IVI software stack.

---

## 4. System Architecture

The simulated architecture consists of the following components:

### User

Initiates an action such as Play, Pause, Resume, Volume Change, or Stop.

### IVI User Interface

Receives the user's input and forwards the corresponding command.

### Media Service

Processes the media command and communicates with the audio subsystem.

### Audio Framework

Creates and forwards the appropriate audio request.

### Audio HAL

Provides the abstraction layer between the Android audio framework and the lower-level audio implementation.

### Audio Driver

Handles the lower-level transfer of audio data.

### Vehicle Speakers

Represent the final audio output.

---

## 5. Example Message Flow

For a Play operation:

```text
User
 ?
IVI UI
 ?
Media Service
 ?
Audio Framework
 ?
Audio HAL
 ?
Audio Driver
 ?
Vehicle Speakers
```

Example simulated log:

```text
IVI UI           | User pressed PLAY button
Media Service    | PLAY command received from IVI UI
Audio Framework  | Creating audio playback request
Audio HAL        | Opening audio output stream
Audio HAL        | Audio output stream initialized
Audio Driver     | Receiving PCM audio data
Vehicle Speakers | Audio output started
```

---

## 6. Technologies Used

* Python
* Pandas
* Matplotlib
* NetworkX
* Google Colab
* GitHub

---

## 7. Project Files

```text
IVI-Media-AudioHAL-Simulation/
¦
+-- IVI_Media_AudioHAL_Simulation.ipynb
+-- README.md
+-- requirements.txt
¦
+-- architecture/
¦   +-- IVI_Message_Flow.png
¦
+-- logs/
¦   +-- simulated_android_logs.txt
¦
+-- results/
    +-- IVI_Message_Statistics.png
```

---

## 8. Results

The project generates:

1. An IVI system architecture diagram.
2. Simulated Android-style system logs.
3. Message statistics for the different components.
4. Event analysis for the simulated operations.

The generated outputs demonstrate how a user command propagates through the IVI media stack before reaching the vehicle audio output.

---

## 9. How to Run

The project can be executed using Google Colab.

1. Open the `.ipynb` file in Google Colab.
2. Install the required Python libraries.
3. Run the notebook cells.
4. Observe the generated message-flow diagram, logs, and statistics.

Required libraries are listed in `requirements.txt`.

---

## 10. Conclusion

This project provides a simplified simulation of message propagation within an IVI audio system. It demonstrates how user input is converted into media commands and propagated through the Media Service, Audio Framework, Audio HAL, and lower-level audio components.

The simulation provides a practical representation of the interaction between the different layers of an IVI audio architecture.
