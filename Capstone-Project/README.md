# Anomaly Detection of Cyber Intrusion

## Introduction

With the ever improving networking technologies, our world is now more
connected than ever. The number of internet users has been growing
exponentially every year and is increasing at a high pace as you read.[^1]


This advancement leads to the greater possibilities in areas such as the
Internet of Things (IoT). IoT are any devices with the capability to be
connected to the internet. It can be your fitness tracker, the
self-driving car, a smart home appliance or even heart monitor implants.
It is predicted that by 2020, there will be 200 billion 'smart' devices
around.

IoT is becoming a commonplace in most parts of our life and as such our
reliance on them increases the value of hacking.

It is therefore of paramount importance that the cybersecurity field
grows along as well.

## Objective

As my capstone project for the Data Science Immersive Course I partake
under General Assembly, I will explore the effectiveness of machine
learning techniques on detecting cyber threats via networking traffic
flows data.

The main goal is to be able to detect most of the cyber threats (meaning
a high recall rate for the hostile traffic flows). The secondary goal is
then to make sure that there's as little false alarms as possible (high
precision rate).

## Dataset

The Intrusion Detection Evaluation Dataset (CICIDS2017) was obtained
from University of New Brunswick.

It contains **15 types of labelled flows** (Benign and up-to-date common
attacks) and approximately **2.8 mil rows** and **85 columns** consisting of
**forward flows** (Network flow from initiator to destination) and **backward flows**
(Network flow from destination back to initiator).

Most of the features can generally be grouped into the following:

1.  **IP Addresses --** Source\_IP, Destination\_IP

2.  **Ports --** Source\_Port, Destination\_Port

3.  **Transport Protocol (TCP:6, UDP:17) -** Protocol

4.  **Number of packets --** Total\_Fwd\_Packets, Total\_Backward\_Packets, Subflow\_Fwd\_Packets, Subflow\_Bwd\_Packets, Flow\_Packets\_persec, act\_data\_pkt\_fwd,

5.  **Packet Size --** Total\_Length\_of\_Fwd\_Packets,
    Total\_Length\_of\_Bwd\_Packets, Fwd\_Packet\_Length\_Max,
    Fwd\_Packet\_Length\_Min, Fwd\_Packet\_Length\_Mean,
    Fwd\_Packet\_Length\_Std, Bwd\_Packet\_Length\_Max,
    Bwd\_Packet\_Length\_Min, Bwd\_Packet\_Length\_Mean, Bwd\_Packet\_Length\_Std,
    Flow\_Bytes\_persec, Subflow\_Fwd\_Bytes, Subflow\_Bwd\_Bytes,
    Min\_Packet\_Length, Max\_Packet\_Length, Packet\_Length\_Mean,
    Packet\_Length\_Std, Packet\_Length\_Variance,
    Average\_Packet\_Size, min\_seg\_size\_forward,
    Init\_Win\_bytes\_forward, Init\_Win\_bytes\_backward

6.  **Packet Header Size --** Fwd\_Header\_Length, Bwd\_Header\_Length

7.  **Flow Duration --** Flow\_Duration

8.  **Amount of time a flow was active before going idle --**
    Active\_Mean, Active\_Std, Active\_Max, Active\_Min

9.  **Amount of time a flow was idle before becoming active --**
    Idle\_Mean, Idle\_Std, Idle\_Max, Idle\_Min

10. **Inter Arrival Time (time between 2 packets sent) --**
    Flow\_IAT\_Mean, Flow\_IAT\_Std, Flow\_IAT\_Max, Flow\_IAT\_Min,
    Fwd\_IAT\_Total, Fwd\_IAT\_Mean, Fwd\_IAT\_Std, Fwd\_IAT\_Max,
    Fwd\_IAT\_Min, Bwd\_IAT\_Total, Bwd\_IAT\_Mean, Bwd\_IAT\_Std,
    Bwd\_IAT\_Max, Bwd\_IAT\_Min

11. **TCP flags** **(TCP flags are used within TCP packet transfers to
    indicate a particular connection state or provide additional
    information) --** Fwd\_PSH\_Flags, Bwd\_PSH\_Flags, Fwd\_URG\_Flags,
    Bwd\_URG\_Flags, FIN\_Flag\_Count, SYN\_Flag\_Count,
    RST\_Flag\_Count, PSH\_Flag\_Count, ACK\_Flag\_Count,
    URG\_Flag\_Count, CWE\_Flag\_Count, ECE\_Flag\_Count

12. **Flow labels --** Label 
    (The 15 labels are: BENIGN, FTP-Patator, SSH-Patator, DoS slowloris, DoS Slowhttptest, DoS Hulk, DoS GoldenEye, Heartbleed, Web Attack -- Brute Force, Web Attack -- XSS, Web Attack -- Sql Injection, Infiltration, Bot, DDoS , PortScan)

For a more detailed description of each feature, please refer to the
excel file on **my github**.

**Citation:** *Iman Sharafaldin, Arash Habibi Lashkari, and Ali A.
Ghorbani, "Toward Generating a New Intrusion Detection Dataset and
Intrusion Traffic Characterization", 4th International Conference on
Information Systems Security and Privacy (ICISSP), Purtogal, January
2018*