# Install Mosquitto MQTT Broker
1. Update Raspberry pi
```sudo apt update && sudo apt upgrade -y```

3. Install Mosquitto Broker and Client
```sudo apt install -y mosquitto mosquitto-clients```

4. Enable and Start Mosquitto
```sudo systemctl enable mosquitto```
```sudo systemctl start mosquitto```

5. Edit the Mosquitto Configuration File
```sudo nano /etc/mosquitto/mosquitto.conf```

6. Add Listener and Allow Anonymous Connections

At the end of the file, add:
'''listener 1883'''
'''allow_anonymous true'''

6. Save and Restart Mosquitto
'''sudo systemctl restart mosquitto'''

7. Test the connection using an MQTT client like MQTT Explorer or by running:
'mosquitto_sub -h <raspberry_pi_ip> -t test/topic'
