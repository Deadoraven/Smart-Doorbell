# Smart Weather Doorbell
A doorbell that cares for you.
# WEATHER
# HEALTH
# SAFETY
#H2 Project Description
#H3 Design Philosophy
The design philosophy for the product is to have separation of concerns between the software that handles the system and the application that handles user experience.
A simple round-robin schedule of function calls is utilized to get the following benefits:
• Enables adding component’s implementation inside the loop function with ease.
• Makes the debugging process easier.
• (Complete product) Separation of front and back ends of the software.
Additionally, the communication design philosophy for the product is to separate the communications between the master and slave (Zigbee), and the master and terminal (Wi-Fi). These provides the following benefits:
• Additional slave devices can be added without affecting Wi-Fi functionality.
• Master able to provide services to multiple terminals using Wi-Fi.
• Master able to provide services to a remote terminal using internet.
• (Low user requirement) Compatible with any device with a browser.
Notable Algorithms
Other than the simple round-robin scheduling, our communication protocol ensures reliable transmission of data between devices and terminal.
Master-Slave Communication (Zigbee)
The communication between master and slave are done with a proper handshake using characters to represent SYN and ACK flags, while termination of communication is done using a character representing a FIN flag. This protocol is similar to TCP and enables the master and slave devices to ensure reliable communication with the addition of timeouts to prevent deadlocks. The timeout timer also enables the device to recover and to be able to serve the user with a small amount of delay that is not noticeable to the user.

Project Description
</body>
</http>
