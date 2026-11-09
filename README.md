INTRODUCTION

This activity focuses on using the WiFiManager library with an ESP32-S3 to connect to a Wi-Fi network. Instead of manually entering Wi-Fi credentials in the code, WiFiManager provides a configuration page where users can select a network and enter its password. The activity also demonstrates how to reset saved Wi-Fi settings, change the access point name, and connect to different networks.

OBJECTIVES

At the end of this activity, you should be able to:

- Install and use the WiFiManager library in Arduino IDE.

-  Configure an ESP32-S3 to connect to a Wi-Fi network.

- Access the Wi-Fi configuration page using a mobile phone.

- Reset saved Wi-Fi credentials using the BOOT button.

- Change the access point name through the code.

- Connect the ESP32 to another Wi-Fi network without changing the program.

Materials Used

- ESP32-S3 Development Board

- USB data cable

- Computer or laptop

- Arduino IDE

- WiFiManager library by tzapu

- Smartphone

- Available Wi-Fi connection or mobile hotspot

Setup Configuration

1. Connect the ESP32-S3 board to the computer using a USB cable.

2. Open Arduino IDE and install the WiFiManager library by tzapu through the Library Manager.

3. Select ESP32S3 Dev Module as the board and select the correct COM port.

4. Add the required Wi-Fi and WiFiManager libraries to the program.

5. Set the access point name to BCA188-ESP32-2024-2220.

6. Configure the BOOT button to reset the saved Wi-Fi settings when held for 3 seconds.

7. Set the Wi-Fi configuration portal timeout to 300 seconds.

8. Upload the program to the ESP32-S3.

9. Open the Serial Monitor and set the baud rate to 115200.

10. Connect a smartphone to the ESP32 access point and open http://192.168.4.1 to access the Wi-Fi configuration page.

BCA188-ESP32-2024-2220

<img width="547" height="581" alt="Screenshot 2026-11-09 190955" src="https://github.com/user-attachments/assets/17b4eefc-1ce6-4c2e-ae16-9d7077731275" />

Wi-Fi Manager Setup Page

<img width="720" height="1056" alt="f1c87b9b-f426-4720-9b5d-043b0408f39c" src="https://github.com/user-attachments/assets/c3a0937b-7daa-4096-84f6-847cb4f17934" />

 Serial Monitor

 <img width="739" height="390" alt="Screenshot 2026-11-09 191646" src="https://github.com/user-attachments/assets/86436673-afcc-4a9c-9c49-8f03b8b33b19" />

 Practice Tasks

Task 1: Test an Incorrect Wi-Fi Password

Entered an incorrect Wi-Fi password to test how the ESP32 responds when the connection fails. The Serial Monitor displayed a connection error.
 
<img width="1901" height="1010" alt="Screenshot 2026-11-09 184800" src="https://github.com/user-attachments/assets/98177572-665e-4553-bb4f-fd0ad33fba1e" />

Task 2: Reset the Saved Wi-Fi Settings

Held the BOOT button for three seconds to clear the saved Wi-Fi credentials. The ESP32 restarted and opened the Wi-Fi configuration portal again.

<img width="1907" height="1012" alt="Screenshot 2026-11-09 195304" src="https://github.com/user-attachments/assets/9b81c98d-6cf2-4d8b-952e-ace738031c56" />

Task 3: Change the Setup Network Name

The setup network name was changed from BCA188-ESP32-2024-2220 to BCA188-ESP32-2024-2220-TEST. After uploading the updated code, the phone's Wi-Fi list was checked to confirm that the new network name appeared.

<img width="720" height="993" alt="fbab140e-da24-468e-82c0-0121a0595bc9" src="https://github.com/user-attachments/assets/d41dc95e-0cf0-409f-b23d-a7744f54e06e" />

<img width="1907" height="1007" alt="Screenshot 2026-11-09 200001" src="https://github.com/user-attachments/assets/05ef837d-ebae-4a16-90ca-0fd4f71cd597" />

Task 4: Connect to a Different Wi-Fi Network

Used a mobile hotspot as the new Wi-Fi network. The ESP32 connected successfully and received an IP address.

<img width="1906" height="1012" alt="Screenshot 2026-11-09 200905" src="https://github.com/user-attachments/assets/032111fc-baa6-421f-852e-d638afbde986" />

Results and Observations

| Task                 | What to do                                                            | What I observed                                                                                                            |
| :------------------: | :-------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------: |
| 1. Wrong Password    | 	Enter a wrong password on the setup page.                            | The ESP32 failed to connect to the selected Wi-Fi network. The Serial Monitor displayed Connect to new AP Failed.          |
| 2.  Reset Settings   | 	Hold the BOOT button for 3 seconds while the board is running.       | The ESP32 cleared its saved Wi-Fi settings and restarted. It started the Wi-Fi Manager again and created its access point. |
| 3. Change the Name   | 	Change the network name, upload, and check your phone’s Wi-Fi list.	 | The access point name was successfully changed to BCA188-ESP32-2024-2220-TEST and appeared in the phone's Wi-Fi list.      |
| 4. Different Network | 	Reset the board, then connect to your phone hotspot.                 | The ESP32 successfully connected to the mobile hotspot and displayed its assigned IP address in the Serial Monitor.        |

Explanation

The board can connect to a different Wi-Fi network without changing the code because WiFiManager saves the Wi-Fi credentials in the ESP32's memory. This allows the board to use the saved credentials or configure a new network without modifying the program.

Conclusion

In this activity, I learned how to use WiFiManager to connect an ESP32 to a Wi-Fi network. I also learned how to reset saved credentials, change the access point name, and connect the board to another network.





