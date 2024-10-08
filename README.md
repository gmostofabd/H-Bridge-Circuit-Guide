# 🎨 **H-Bridge Circuit Guide:** ***Control Your DC Motor Like a Pro*** 🛠️


<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 60%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/1ff3556ab04c3834a8773daedc25ae04b6482cfe/assets/images/H%20BRIDGE%20CIRCUITS%20(NPN)_3.gif" alt="H-Bridge Circuit Diagram" width="80%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">H-Bridge Circuit Diagram</h3>
  <p align="justify" style="color: #555; font-size: 1.5em;">
   The H-Bridge Circuit is essential for controlling the speed and direction of DC motors. It is named after its unique "H" shape configuration and is widely used in robotics, embedded systems, and automation projects. The circuit enables smooth motor rotation in both forward and reverse directions by switching the current flow across the motor.
  </p>
</div>

---

</br>

### ⚡ **Overview**
The **H-Bridge Circuit** is essential for controlling the **speed** and **direction** of **DC motors**. It is named after its unique "H" shape configuration and is widely used in **robotics**, **embedded systems**, and **automation** projects. The circuit enables smooth motor rotation in both **forward** and **reverse** directions by switching the current flow across the motor.

---

</br>


## ✨ **Key Features**
- 🔄 **Bidirectional Control**: Seamlessly switch between **forward** and **reverse** motor rotation.
- 🛠️ **Speed Regulation**: Use **Pulse Width Modulation (PWM)** for fine-grained control over motor speed.
- ⚙️ **Efficient Design**: Built using **MOSFETs** or **BJTs** for optimized performance, making it ideal for both **low-power** and **high-power** applications.

---


</br>




### 🛠️ **Key Considerations for H-Bridge Circuit Design**

1. **Switching Components and Current Capacity**  
   - It's crucial to select transistors or switching components that can handle sufficient current. For example, if your transistor is rated for a maximum of 2 amperes, exceeding this value can cause **damage** to the component.
   
2. **PNP and NPN Transistor Placement**  
   - In the H-Bridge circuit, we typically use **PNP transistors** on the upper side and **NPN transistors** on the lower side for effective current flow and control.

3. **Avoiding Short Circuits**  
   - Be cautious of creating a **short circuit**. Directly switching from **positive to negative** without proper control can **burn out** your circuit and damage electronic components.

4. **Discharging Times & Timing Sensitivity**  
   - When **timing** and **sensitivity** are critical, transistors are preferred over magnetic relays. While magnetic relays are suitable for handling **higher currents**, they are not ideal when precise timing is required.

5. **Voltage Drops Across Switching Components**  
   - Always account for the **voltage drops** across the transistors or relays. This can affect the overall performance of your circuit, especially in low-voltage applications.

---

</br>


### Example: H-Bridge Circuit with Transistors

<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 40%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/c9a6fa3914d6b2e107c8326d4fe7ebf02e52e27d/assets/images/H%20BRIDGE%20CIRCUITS%20(NPN).gif" alt="H-Bridge Circuit Diagram" width="70%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">H-Bridge Circuit with Transistors</h3>
</div>

---

By following these guidelines, you can ensure that your H-Bridge circuit operates safely and efficiently, protecting both your components and your circuit.





---

</br>







### 🛠️ **Locating Transistors in an H-Bridge Circuit**

In an H-Bridge circuit, the **placement of transistors** is crucial for the correct operation of the circuit. As shown in the image above, **PNP transistors** are located at the **upper side** of the circuit, while **NPN transistors** are positioned at the **bottom side**.

---

</br>


### 🔑 **Why is This Placement Important?**

1. **Transistor Symbol and Current Flow**  
   - The **arrow mark** on the transistor symbol always indicates the **emitter** side.
     - For a **PNP transistor**, current flows from **Emitter to Collector**.
     - For an **NPN transistor**, current flows from **Collector to Emitter**.

2. **Connection to the Load**  
   - For **PNP transistors**, since the current flows from the **Emitter to the Collector**, the load (e.g., a motor) should be connected to the **output** side (Collector).
   - For **NPN transistors**, with current flowing from the **Collector to the Emitter**, the load should be connected to the **input** side (Collector).

---

</br>


By placing **PNP transistors on the upper side** and **NPN transistors on the lower side**, you can control the **direction of current flow** and ensure proper operation of the H-Bridge circuit for **bidirectional motor control** or other applications like **inverters** and **power amplifiers**.

<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 50%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/371d179cd57c97ad1d82e3bd396f6d85d30a6f02/assets/images/555_PWM.jpg" alt="H-Bridge Circuit Diagram" width="60%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">H-Bridge Circuit with PNP and NPN Transistors</h3>
</div>

---

This approach ensures efficient current flow management and helps you avoid common pitfalls like incorrect load connections and circuit damage.









### 🔧 **Voltage Requirements and Microcontroller Integration**

When using **microcontrollers**, it's essential to note that most of them output **3.3V** on their digital pins. However, if your motor or load requires a higher voltage (e.g., **12V**), the 3.3V output from the microcontroller won’t be enough.

---

</br>


### 🖥️ **How PNP Transistors Help in Boosting Voltage**

To address this, you can use a **PNP transistor** to supply the needed higher voltage. For example, if your motor requires **12V DC**:
- You can connect a **9V supply** to the **Emitter pin** of the PNP transistor.
- Connect the **microcontroller's 3.3V digital output** to the **Base pin**.
- The result will be **12.3V DC** at the **Collector pin**, which can power your motor or any other load.

This allows you to measure the **12.3V DC** output using a multimeter or directly connect it to a **DC motor**.

<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 50%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/371d179cd57c97ad1d82e3bd396f6d85d30a6f02/assets/images/DC%20Motor%204.jpg" alt="H-Bridge Circuit Diagram" width="60%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">H-Bridge Circuit with PNP and NPN Transistors</h3>
</div>

---

</br>


### ⚠️ **Incorrect NPN Transistor Placement**

If you connect an **NPN transistor** in the same way (to the positive voltage output), the motor won’t work. This is because in the case of the **NPN transistor**, the load (i.e., motor) needs to be connected to the **input** side (Collector), not the **output** side (Emitter).

---

</br>




<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 60%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/0196677bb0e9e28d16f8f74ac4f2d1020e6a2614/assets/images/H%20BRIDGE%20CIRCUITS_a.gif" alt="H-Bridge Circuit Diagram" width="60%" style="border-radius: 8px;">
</div>


### 🔄 **Controlling Motor Rotation**

Once the transistor placement is sorted, you can now focus on **switching** to control the **rotation direction** of the motor. As previously discussed, switching alters the current path, which in turn changes the **rotation direction** of the motor.

For example:
- **Closing Switch 1 and Switch 4** while **Opening Switch 2 and Switch 3** will cause the current to flow in a direction that results in forward rotation of the motor.
  
<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 40%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/5679607545cadf46939de2878cca5b8accee0079/assets/images/H%20BRIDGE%20CIRCUITS_2b.gif" alt="H-Bridge Circuit Current Flow Diagram" width="60%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">Current Flow in H-Bridge Circuit (Switch 1 & 4 Closed)</h3>
</div>

---

</br>


### ⚡ **Preventing Residual Voltages with Diodes**

After the motor has stopped, any **residual voltage** remaining in the circuit needs to be safely dissipated. If not, it could damage your components. This is why we connect **diodes** to create a **return path** for the voltage to flow to **Ground (GND)**.

The diodes protect the circuit by directing the residual voltage safely to GND, ensuring that no lingering charge damages your transistors or other components.

---

This organized flow ensures correct **voltage boosting**, **safe motor operation**, and **circuit protection** from residual voltages, enabling your H-Bridge circuit to function smoothly.




---

</br>


## 🔧 **Types of H-Bridge Circuits**

### 1. **Mechanical H-Bridge** 🕹️
   - **Description**: Relies on **mechanical switches** or **relays** to control motor direction.
   - **Pros**: Simple and easy to implement.
   - **Cons**: **Slower** operation and **shorter lifespan** due to mechanical wear.

### 2. **Transistor-based H-Bridge** 💡
   - **Description**: Uses **BJTs** or **MOSFETs** to electronically switch current.
   - **Pros**: **Fast switching** and **reliable** performance.
   - **Cons**: BJTs are less efficient than MOSFETs.

### 3. **Complementary MOSFET H-Bridge** 🔋
   - **Description**: Combines **N-channel** and **P-channel** MOSFETs for a balanced design.
   - **Pros**: Good balance between **ease of control** and **performance**.
   - **Cons**: **Higher complexity** due to the need for both types of MOSFETs.

### 4. **N-channel MOSFET H-Bridge with Bootstrap** 🏎️
   - **Description**: Uses only **N-channel MOSFETs**, improving efficiency.
   - **Pros**: **Lower on-resistance** for higher efficiency.
   - **Cons**: Requires a **bootstrap circuit** or **gate driver** for high-side switching.

### 5. **IC-based H-Bridge** 🎛️
   - **Description**: Fully integrated into an **IC** (e.g., **L298N**, **L293D**).
   - **Pros**: **Compact** and **easy to use** with built-in protection features.
   - **Cons**: Limited to **low-power** applications.

---

</br>

## 📌 **Why Use BJTs or MOSFETs in H-Bridge Circuits?**

### **1. Bipolar Junction Transistor (BJT)** H-Bridge

#### **Advantages:**
- **Simplicity**: BJTs are relatively easy to control using base current, requiring lower gate drive circuitry.
- **Cost-Effective**: BJTs are generally cheaper than MOSFETs, making them suitable for **low-cost** applications.
- **Saturation Mode**: In **saturation mode**, BJTs can handle a moderate amount of current, making them usable in low to moderate power circuits.

#### **Disadvantages:**
- **Higher Power Loss**: BJTs have higher **switching losses** and **voltage drop** when conducting (due to V_CE saturation), leading to reduced efficiency.
- **Slower Switching Speed**: Compared to MOSFETs, BJTs have **slower switching times**, which limits their use in high-speed applications like PWM control.
- **Base Drive Current**: BJTs require continuous **base current** to remain in the on-state, which increases power consumption in control circuits.

#### **Best For**:
- **Low-power applications** where simplicity and cost are more important than efficiency.

---
</br>

### **2. Metal-Oxide-Semiconductor Field-Effect Transistor (MOSFET)** H-Bridge

#### **Advantages:**
- **High Efficiency**: MOSFETs have **lower on-resistance (R_DS(on))**, resulting in **lower conduction losses** and higher efficiency.
- **Fast Switching**: MOSFETs can switch on and off much faster than BJTs, making them ideal for high-frequency **PWM control**.
- **Voltage-Controlled**: Unlike BJTs, MOSFETs are controlled by **voltage** at the gate, requiring minimal current to switch on, thus reducing control power consumption.
- **Higher Power Capability**: MOSFETs are better suited for **high-power** applications due to their low switching losses and high-speed switching.

#### **Disadvantages:**
- **Gate Drive Circuit**: MOSFETs, especially **N-channel** MOSFETs, require a more complex gate drive circuit, particularly for **high-side switching**. A **bootstrap circuit** or specialized **gate driver** IC is often required.
- **Cost**: Generally, MOSFETs are more expensive than BJTs, especially **low R_DS(on)** models.
- **Static Sensitivity**: MOSFETs are more susceptible to **static damage** due to their high input impedance.

#### **Best For**:
- **High-power** or **high-efficiency** applications where **fast switching** and low power loss are crucial, such as in robotics, electric vehicles, and industrial systems.

---


</br>


## 🛠️ **Applications**

- 🤖 **Robotics**: Powering motors for robot movement.
- 🚗 **Electric Vehicles**: Control of DC motors in small EV projects.
- 🏭 **Automation Systems**: Industrial systems requiring precision motor control.
  
---

</br>



# 🎨 **Full Bridge Sine Inverter Circuit Guide:** ***Transform Your DC to AC Power with Ease*** ⚡

<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 50%; margin: auto;">
  <img src="https://example.com/full_bridge_inverter.gif" alt="Full Bridge Inverter Circuit Diagram" width="60%" style="border-radius: 8px;">
  
  <h3 style="margin-top: 20px;">Full Bridge Inverter Circuit Diagram</h3>
  <p align="justify" style="color: #555; font-size: 1.5em;">
   A Full Bridge Sine Inverter converts DC voltage to AC voltage using four switching devices arranged in a bridge configuration. This inverter design allows for efficient operation and can provide a pure sine wave output, making it suitable for various applications, including powering AC loads from a DC source.
  </p>
</div>

---

</br>

### ⚡ **Overview**
The **Full Bridge Sine Inverter** is a type of inverter that utilizes a configuration of four switches (MOSFETs or IGBTs) to convert DC power into AC power. This design enables the generation of a sine wave output, which is crucial for powering sensitive electronic devices and appliances.

---
</br>


## 📝 **Resources and Links**
- [🔗 Full Bridge Inverter Operation Explanation](https://example.com/full-bridge-inverter-guide) <!-- Replace with actual link -->
- [🔗 PWM Control Techniques](https://example.com/pwm-control) <!-- Replace with actual link -->

---

</br>


### **Example Full Bridge Inverter Simulation**
![Full Bridge Inverter Simulation](https://example.com/full_bridge_inverter_simulation.gif) <!-- Replace with actual image or GIF link -->

---

</br>











## 📐 **Circuit Diagram** 

```plaintext
         +V
          |
      +---+---+
      |       |
    [S1]     [S2]  
      |       |
     MOTOR    MOTOR
      |       |
    [S3]     [S4]
      |       |
      +---+---+
          |
         GND
```

</br>

**Explanation**:
- **S1 & S4** ON → **Forward Rotation**
- **S2 & S3** ON → **Reverse Rotation**

---

</br>

## 🔑 **Keywords**
`H-Bridge | DC Motor Control | Transistor-based H-Bridge | MOSFET H-Bridge | Robotics | PWM Control | Motor Driver | Embedded Systems`

---


<
</br>


### **Example H-Bridge Circuit Simulation**
![H-Bridge Simulation](https://example.com/h-bridge-simulation.gif) <!-- Replace with actual image or GIF link -->

---

</br>


## 📝 **Number of control line inputs in an H-Bridge circuit**

The number of control line inputs in an H-Bridge circuit significantly impacts its functionality, control complexity, and flexibility. Here’s a breakdown of how using different numbers of control lines—such as 2, 4, or even more—affects the operation of the H-Bridge:





### 1. **Single Input Control**


#### Functionality
A single input can be used to control the H-Bridge to achieve basic functionalities, often through specific configurations or additional circuitry. Here are a couple of methods:

1. **Using a Dual-Function Signal (PWM)**:
   - A single PWM input can control both the direction and speed of the motor. 
   - For instance, you could program a microcontroller to determine the direction based on the duty cycle of the PWM signal:
     - **Duty Cycle < 50%**: Motor rotates in one direction (e.g., forward).
     - **Duty Cycle = 50%**: Motor stops.
     - **Duty Cycle > 50%**: Motor rotates in the opposite direction (e.g., reverse).
   - This approach provides speed control via the PWM signal while maintaining direction control.

2. **Using an H-Bridge Driver IC**:
   - Many H-Bridge driver ICs can accept a single input signal to control motor direction. They may internally handle direction based on additional logic:
     - The IC may include built-in logic that interprets the input signal to determine the direction and speed.
     - For example, the input could be high for one direction and low for the other direction, while PWM could control speed.

3. **Using Logic Levels**:
   - With additional circuitry, a single control signal can be modified using logic gates or relays to achieve the desired motor control.
   - For instance, an inverter could be used to toggle the control lines of the H-Bridge based on the state of a single input.

### Advantages of Single Input Control
- **Simplicity**: Reduces the number of required inputs, making the control scheme simpler and easier to implement.
- **Less Wiring**: Fewer control lines mean reduced complexity in wiring, which can simplify prototyping and assembly.
- **Cost-Effective**: A single input solution can reduce the need for additional components or more complex controllers.

### Disadvantages
- **Limited Functionality**: Using a single input may limit the ability to implement advanced features like braking or separate speed control without additional complexity.
- **Complex Logic**: The logic required to determine direction and speed from a single input can become complex, especially in software.

### Summary
While traditional H-Bridge configurations use multiple control inputs for flexibility and advanced control, a single input can effectively control an H-Bridge circuit for basic operations. This method is especially useful in simple applications or where design simplicity and cost-effectiveness are priorities.

---

</br>



### 2. **Two Control Inputs (Basic Control)**

#### Functionality:
- **Forward and Reverse Operation**: With only two control inputs, you can control the direction of the motor. For example, one input can be for forward rotation and the other for reverse rotation.
- **Stop Function**: Typically, if both inputs are low, the motor stops. 

#### Advantages:
- **Simplicity**: Fewer control inputs make the design simpler, easier to implement, and less prone to errors.
- **Lower Complexity**: The circuit requires minimal logic, making it straightforward to use with basic microcontrollers or switches.

#### Disadvantages:
- **Limited Functionality**: Only basic operations (forward, reverse, and stop) can be achieved, with no speed control.

---

</br>


### 3. **Four Control Inputs (Enhanced Control)**

#### Functionality:
- **Forward, Reverse, and Brake**: Each of the four inputs controls one switch in the H-Bridge, allowing for more sophisticated operations:
  - Input 1 and Input 4 ON: Forward rotation
  - Input 2 and Input 3 ON: Reverse rotation
  - Input 1 and Input 2 ON: Brake (if both are enabled)
  - Input 3 and Input 4 ON: Brake (if both are enabled)
  - All inputs low: Motor stops

#### Advantages:
- **Greater Control**: You can easily implement additional functionalities like braking and coast (allowing the motor to spin down naturally).
- **Speed Control via PWM**: If the inputs are also PWM signals, speed control becomes feasible.
- **Increased Flexibility**: More control inputs allow for easier integration with more complex control schemes (e.g., joystick control).

#### Disadvantages:
- **Complexity**: More control inputs lead to increased complexity in design and programming.
- **Risk of Short Circuits**: If not properly managed, activating certain combinations of inputs can lead to short circuits or shoot-through conditions.

---


</br>


### 3. **More than Four Control Inputs (Advanced Control)**

#### Functionality:
- **Advanced Features**: Using additional control lines can enable even more features, such as:
  - Synchronized control of multiple motors.
  - Diagnostics and status feedback (e.g., current sensing).
  - Integration with more sophisticated control algorithms (e.g., PID control).

#### Advantages:
- **Fine-Grained Control**: More options for control can lead to advanced functionalities, including smoother speed control, torque control, and coordination between multiple motors.
- **Enhanced Features**: Additional functionalities like speed feedback, thermal shutdown, and error detection can be implemented.

#### Disadvantages:
- **High Complexity**: More control lines complicate both the hardware design and software implementation.
- **Increased Cost**: More components may be needed, leading to higher costs and potentially increased power consumption.

### Summary
In summary, the number of control lines in an H-Bridge circuit directly influences how the circuit operates, the complexity of the control logic, and the range of functionalities that can be implemented. 

- **2 Control Inputs**: Simple, basic control (forward/reverse/stop).
- **4 Control Inputs**: More functionalities like braking and speed control; allows for a richer user experience.
- **More than 4 Control Inputs**: Supports advanced features and better control schemes, but increases complexity and costs.

Choosing the appropriate configuration depends on the specific application requirements, the desired level of control, and the complexity you're willing to manage in both hardware and software.

---
/br>

## 📝 **Resources and Links**

- [🔗 L298N Motor Driver IC Datasheet](https://example.com/L298N-datasheet) <!-- Replace with actual link -->
- [🔗 Introduction to Motor Control](https://example.com/motor-control-guide) <!-- Replace with actual link -->

---


</br>




## 📚 **Tutorials on this Topic**


1. **[SparkFun: H-Bridge Basics](https://learn.sparkfun.com/tutorials/h-bridge-motor-control)**  
   - Covers the fundamentals of H-Bridge circuits for DC motor control.

2. **[Electronics Hub: H-Bridge Motor Driver](https://www.electronicshub.org/h-bridge-dc-motor-driver-circuit/)**  
   - Detailed guide on building and using H-Bridge circuits.

3. **[RobotShop: DC Motor Control](https://www.robotshop.com/community/tutorials/show/dc-motor-control-using-an-h-bridge)**  
   - Comprehensive motor control tutorial with H-Bridge circuits for robotics.

4. **[All About Circuits: H-Bridge Theory](https://www.allaboutcircuits.com/technical-articles/h-bridge-theory-and-practice/)**  
   - Explains the theory and practical application of H-Bridge motor control.

5. **[Texas Instruments: H-Bridge Fundamentals](https://www.ti.com/lit/an/slva500/slva500.pdf)**  
   - Application note on H-Bridge design and motor control techniques.

These resources offer practical and theoretical insights into H-Bridge circuits for motor control.


---

</br>


## 📚 **References**

1. **Li, Z., & Rahman, K. M. (2008).** *H-Bridge Based Power Converter for High Performance Motor Control*.  
   - This paper discusses advanced control techniques for DC motors using H-Bridge power converters, focusing on efficiency and thermal management.
   - [Read the Paper](https://ieeexplore.ieee.org/document/4637254)  
  
2. **Jahns, T. M. (1994).** *Controlled Rectifier Inverters and DC Motor Drives: A Unified Control Strategy*.  
   - A foundational paper on using rectifier inverters for DC motor control with H-Bridge topology, highlighting control strategies and performance optimization.
   - [Read the Paper](https://ieeexplore.ieee.org/document/473243)  
  
3. **Vasquez, J., Guerrero, J. M., & Lopez, J. (2011).** *Adaptive Control Techniques for H-Bridge Motor Drive Systems*.  
   - Explores adaptive control algorithms applied to H-Bridge circuits for enhanced DC motor control, particularly in varying load conditions.
   - [Read the Paper](https://ieeexplore.ieee.org/document/6032228)  
  
4. **Marwan, A., & Harb, M. (2019).** *PWM Techniques in H-Bridge Inverter Circuits for DC Motor Drives*.  
   - A comprehensive study on the application of Pulse Width Modulation (PWM) in H-Bridge circuits to improve motor performance and efficiency.
   - [Read the Paper](https://www.sciencedirect.com/science/article/pii/S0196890419304567)  
  
5. **Choi, H. H., & Chung, W. Y. (2006).** *Sensorless Control of DC Motors Using H-Bridge Inverter Circuits*.  
   - Focuses on sensorless control strategies for DC motors with H-Bridge circuits, aiming to reduce system cost and complexity.
   - [Read the Paper](https://ieeexplore.ieee.org/document/4125962)  
  
6. **Lee, C. M., & Park, S. Y. (2015).** *H-Bridge Based Control of Brushless DC Motors for Electric Vehicles*.  
   - This paper looks at the application of H-Bridge motor control in electric vehicle systems, with an emphasis on efficiency and regenerative braking.
   - [Read the Paper](https://www.journalofenergy.com/article/1009387)

7. **Sabanovic, A., & Sabri, H. (2017).** *Sliding Mode Control for H-Bridge DC Motor Drives*.  
   - The paper introduces advanced control methodologies like sliding mode control to improve the performance of DC motors controlled via H-Bridge circuits.
   - [Read the Paper](https://link.springer.com/chapter/10.1007/978-3-319-67362-4_16)

---




<div align="center" style="border: 2px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; width: 60%; margin: auto;">
  <img src="https://github.com/gmostofabd/H-Bridge-Circuit-Guide/blob/af3ed22c99e6b4c4dda2b82cd099a4f8e237fb85/assets/images/H%20BRIDGE%20CIRCUITS.gif" alt="H-Bridge Circuit Diagram" width="80%" style="border-radius: 8px;">
  <h3 style="margin-top: 20px;">H-Bridge Circuit Diagram</h3>
  <p align="justify" style="color: #555; font-size: 1.5em;">
   The H-Bridge Circuit is essential for controlling the speed and direction of DC motors. It is named after its unique "H" shape configuration and is widely used in robotics, embedded systems, and automation projects. The circuit enables smooth motor rotation in both forward and reverse directions by switching the current flow across the motor.
  </p>
</div>
