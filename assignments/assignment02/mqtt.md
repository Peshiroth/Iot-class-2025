# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output
[15:28:12] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [15:28:12] DEBUG | Received CONNACK (0, 0)
Hi!!!!
Enter QoS level (0, 1, 2): 2
[15:28:26] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301044/temperature'', ... (6 bytes)
[15:28:26] PUBLISH REQUESTED | QoS=2 | Message='Hi!!!!' | msgid=1
Enter message to publish: [15:28:26] DEBUG | Received PUBREC (Mid: 1)
[15:28:26] DEBUG | Sending PUBREL (Mid: 1)
[15:28:26] DEBUG | Received PUBCOMP (Mid: 1)
[15:28:26] PUBLISHED | msgid=1

## Subscriber_qos.py Output
[15:27:26] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[15:27:26] DEBUG | Received CONNACK (0, 0)
[15:27:26] Connected with result code 0
[15:27:26] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301044', 2)]
[15:27:26] DEBUG | Received SUBACK