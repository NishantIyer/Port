---
title: About
description: About Portena
image: https://cdn.discordapp.com/attachments/971299427715272734/1114144376311001168/Nishant_Iyer.png
plum: false
---
# Portena: Revolutionizing Remote Computing

Working as a volunteer for Cardano, I had to work on HPC (High-Performance Computing) markets, analyze them and develop custom marketplace images to share with the community. Whilst monitoring an HPC instance in Singapore, a thought ignited my curiosity: How much computing power is truly required to establish a remote connection to a desktop instance? To my astonishment, the RDP (Remote Desktop Protocol) task consumed a mere 10MB of RAM. This revelation piqued my interest as industry giants like VMware and Citrix presented DaaS (Desktop as a Service) and remote desktop solutions as alternatives, yet they necessitated a fully-fledged $500 computer. It struck me then: Why not create a diminutive microcontroller capable of serving as a client for a remote instance? And thus, the concept of Portena was born.

Our computational needs are often discrete, fluctuating between full capacity and merely a fraction thereof. Consider the scenario of an office employee utilizing a computer armed with 8GB of RAM and a quad-core processor; their computational requirements oscillate like a variable "x." At times, "x" may hover around 40%, while on other occasions, it might dwindle to a mere 10%. Regrettably, the surplus computing resource remains idle, going to waste.

Portena is meticulously designed to bridge this gap by connecting a small Single Board Computer (SBC) to a cloud server, mirroring its activities seamlessly on a desktop screen via an HDMI cable. Furthermore, Portena incorporates all the essential peripherals to empower users with effortless control over their Hybrid PCs. To establish the remote connection, I have developed a specially tailored protocol called uNet. Constructed upon TCPv8, uNet harnesses cutting-edge algorithms, ensuring high transmission rates with minimal latency. This protocol operates even in regions with limited internet connectivity, guaranteeing accessibility for users across the globe. Currently, I a, fully immersed in the prototyping phase, using the popular ESP32 microcontroller to develop a client-side solution while simultaneously working on the server-side implementation.

Portena's remote connection is facilitated through CoaaS (Compute-as-a-Service) infrastructures dispersed globally. These serverless models offer scalable "balloon-like" functions/containers that can be dynamically expanded or contracted to meet demand. Moreover, I have devised a distinctive plugin for each Portena instance, aptly named DRATP (Dynamic Resource Allocation and Task Prioritization). DRATP leverages AI/ML algorithms to optimize resource allocation and pricing, leading to cost reductions of up to 80%, as substantiated by my comprehensive tests.

![Portena Image](https://media.discordapp.net/attachments/971299427715272734/1117070920721371289/sirg.png?width=395&height=491)

Portena is still in its nascent ideation stages, and I have been ardently engrossed in prototyping, rigorous testing, and extensive research. For further insights into the remarkable technologies it embodies, please look at the blog section on our website.

If you are interested and eager to learn more about Portena or wish to get in touch, kindly reach out to me at [nishant.iyer62@gmail.com](mailto:nishant.iyer62@gmail.com). I would be delighted to engage in a profound discussion about this visionary project.
