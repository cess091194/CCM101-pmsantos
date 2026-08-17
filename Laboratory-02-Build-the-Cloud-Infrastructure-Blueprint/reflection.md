# Reflection

Among all four cloud infrastructure components explored in this activity, I believe networking is the most important. Compute resources and storage capacity mean little without a reliable network connection. The system needs that connection to be accessible to users and to communicate with other cloud services. This became clear during my investigation of the KillerCoda server. I retrieved the hostname and IP address as part of the networking layer. Without these, there would be no way to reach the server from outside.

Linux also plays a major role in supporting cloud computing. Most cloud servers today are Linux-based, including the one used in this activity. In my case, I worked on Ubuntu, which is a distribution of Linux. Through terminal commands, I was able to investigate the server's compute, storage, and networking configuration directly. I did not need a graphical interface to do this. This shows why Linux serves as such a strong foundation for cloud environments.

Technical documentation is also essential before deploying infrastructure because it serves as a guide and reference for the entire team. Without clear documentation, it would be difficult for other engineers to understand the setup. It would also be harder to troubleshoot issues or justify the design decisions that were made.

Throughout this activity, I learned several new skills. The main one was using different Linux commands to investigate system information. One challenge I encountered was that the `lscpu` command did not work on the server. I had to use an alternative command, `cat /proc/cpuinfo`, to retrieve the CPU model information instead. I also learned how to properly format technical documentation in Markdown and how to use Draw.io to create a diagram.

Overall, I feel that my GitHub Cloud Computing Portfolio has become more structured and professional after completing this activity. I now have an added technical report, comparison table, and visual diagram. These all demonstrate my understanding of cloud infrastructure.
