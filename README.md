# Automatic Supervision Application - An interface for a task supervision system. 

This is an application that provides a user-friendly graphical user interface for a supervision syetem. The application ` ASAp_Automatic_Supervision_Application.ipynb ` launches the interface. The folder ` assets ` is required for proper functionality of the application. This application uses the supervision system in ` SupervisionSystem.maude `, which has to be in the same folder as the application. 

The folder ` Example task patterns ` contains patterns and sequences for other task examples that can be uploaded to the supervision system: Spanish course on a learning platform, tea preparation, salad preparation. The folder also contains various sequences that can also be uploaded to the supervision system. This folder also contains a script for converting DISCO .XML process maps to compatible .json files that can be uploaded to the supervision system. 

The folder ` Screenshots ` contains screenshots for a sample task supervision. 

# Launching the application

In order to use the application, it is sufficient to launch the file ` ASAp_Automatic_Supervision_Application.ipynb `, which launches a web server with the application. Some ` .ipynb ` editors immediately launch an instance of the application in the editor, but it can also be opened from the browser.  The user interface is accessible from any modern browser at the address ` https://localhost:8050 `. In case port 8050 is not available, the next available port will be used. An arbitrary address and port can also be defined in the source code of the application. In order to make the application available from the network, the address which the program should be accessible from can be specified. The code contains an example for the address 192.168.0.102 and the port 8053. Once the application is launched, it utilises the given port and that port becomes unavailable.

Several instances of the application can be opened while the python prorgram is running. These instances run independent and different supervision procedures can be performed simultaneously and independently. The states of the application are saved in the browser session while the session is active.

# Interface

The interface is divided into two main parts – the interactive pattern area (on the left) and the control panel (on the right). 

![The general user interface](https://github.com/supervision-systems-development/supervision_system_interface/blob/main/Images/generalUserInterface-6040.png)

The **interactive pattern** area shows the current task model as an interactive pattern. For convenience, pattern nodes can be dragged to any position on the interactive area in order to make the pattern more user-friendly. Similarly, patterns can be selected (by a mouse click) and deselected (by a click) in order to make the application more explainable. 

In addition to representing the task model, the interactive pattern displays the supervision progress. The progress is shown by green highlights of "executed" node actions and yellow highlight of "blocked" nodes. The colour highlighting of the interactive pattern represents the supervision indicators. This assists the user during supervision (by showing the executed actions, the blocked actions and also makes it easier for the user to intuitively learn the sequence of actions by noticing the actions that have not been executed yet next to the executed (green) actions. 

The pattern is a Dependency Graph with added node functions that extend the functionality of the dependency graph. 

The **control panel** allows the user to perform various activities with the pattern, the sequence and the supervision.

The control area is divided into three main modules: The Editing Module, the Supervision Module and the Example Repository Module. The control area is divided into tabs, with each module having at least one corresponsing tab that allows the user to navigate to it. 

The editing module has two assigned tabs – the "Edit Pattern" and the "Edit Sequence" tabs. The supervision module has one tab assigned – "Supervision", and the example repository module has one tab – the "Example Repository". 

The **"Edit Pattern" tab** gives the user access to the **editing module** allows the user to **edit the pattern** by adding nodes, removing nodes, resetting the pattern, changing node functions and adding edges. 

The **"Edit Sequence" tab** gives the user access to the **editing module** and allows the user to edit the sequence either by manually adding the action labels separated by a comma or by interactively adding the sequence by clicking nodes corresponding to each action in the desired order. 

The **"Supervision" tab** gives the user access to the **supervision module** and allows the user to perform automatic supervision. Automatic supervision can be performed either by using an already existing complete sequence of actions of a task, by showing the supervision step by step for each action or performing the entire supervision at once and showing the end result. Alternatively, conformance checking can be performed, which doesn't assess the supervision performance in general, but rather checks, whether the sequence conforms to the pattern fully, partially or not at all. The supervision results are shown in their corresponding fields with corresponding labels. 

The **"Examples Repository tab** gibes the user access to the **examples repository module** and allows the user to select previously made example patterns and example sequences. The examples repository contains sequences from the JIGSAWS dataset and patterns based on prior work with added node functions. Additionally, the repository contains examples used in the paper which can be selected and the results from the paper can be replicated. 

In order to terminate the application instance, it is sufficient to close the browser tab. Closing the browser tab will not terminate the python program that initialiizes these instances. In order to terminate the pythong program, it is sufficient to terminate the python program. 

 









