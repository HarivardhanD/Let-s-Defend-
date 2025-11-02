# VOIP

### Your close friend James recently received a suspicious phone call from someone claiming to be his bank. The caller asked for sensitive information, making James uneasy. Suspecting a potential Vishing (Voice Phishing) attack, you decide to investigate by capturing and analyzing the VoIP traffic.

- So i was given a set of question in here and will be solving each of them one by one 

1)  First lest understand what VOIP is ?
=> it means making phone calls using the internet instead of a regular phone line

- Normally, when you make a phone call, your voice travels through telephone wires.

- With VoIP, your voice is turned into digital data and sent over the internet — just like an email or a video.
exapmple : whatsapp, insta calls

2) what is RTP packets ?
=> Your voice is recorded by the microphone.

- It’s converted into digital data and split into tiny chunks called packets.

- Each chunk is wrapped in an RTP packet, which contains:

    - A timestamp (to keep the order of the sound right)

    - A sequence number (so lost packets can be detected)

    - The audio data (your voice)

3) How many RTP packets were in the traffic?
- For solving this i went to WIRESHARK and then in packet search , i wrote RTP and then when i scrolled and saw bottom , i saw it showed number of RTP packets => 18348

4) When did the fake call with James start?
Answer Format: YYYY-MM-DD HH:MM:SS (UTC)
=> For this all i did was went to, VIEW -> TIME -> THEN CLICK DATE AND TIME, U WILL GET THE ANSWER => 2024-05-03 20:36:36

5) what is the SIP protocol?

The Session Initiation Protocol (SIP) is a communication protocol used to establish, manage, and terminate voice or video calls over IP networks. It handles the signaling part of VoIP — like starting a call, ringing, and ending it — while protocols like RTP handle the actual media transmission.

6)  What is the Jame’s phone number?
=> Here, we’ll need to use the sip filter to find the phone number., i went to SIP packes and there i found from and to address where we had a following format : ` < sip phone_numb@ip_address> ` , so answer is => 7001

7) How long was the call with the bank?
=> For this one, i went to telephony setting and VOIP section , there i found the time duration => 00:01:35

8)  What is the phone number of the bank that James received a call from?
=> Same as quest 6 => 01326947697

- for the next 2 questions i had to listen to the audio , since i could not listen to the audio on the current server , what i did was, as instructed , logged in using RDP and then went to wireshark , telephony -> VOIP call and then on the packet, i click play stream and listen and hence i got the solution
