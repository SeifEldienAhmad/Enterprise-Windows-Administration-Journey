# Explaining the Processes Found in the Memory Checking task

| Process | What the process do |
|----------|--------------------:|
| MsMpEng.exe | the core executable for Microsoft Defender Antivirus. Its primary job is to perform real-time threat scanning, monitor your system for malicious software, download protection updates, and protect your computer in the background. |
| SearchUI.exe | a core Windows process that powers the search bar, Start Menu search, and the Cortana assistant |
| svchost.exe (LocalSystemNetwork) | a core Windows container that runs multiple critical background services requiring network access. It groups related services to conserve system memory and isolates them for security |
| backgroundTaskHost.exe | an essential Windows component responsible for running background tasks and services. It acts as a bridge, allowing Microsoft apps and virtual assistants (like Cortana) to execute background operations like checking the weather, fetching notifications, or searching files |
| explorer.exe | the core Windows process that powers your graphical user interface (GUI). It manages your desktop, Start menu, taskbar, and File Explorer. Without it running, you would only see a blank screen instead of your usual icons and folders |
| dwm.exe | a core Windows system component that renders your graphical user interface. It is responsible for drawing your desktop, managing visual effects like window transparency and animations, and handling high-resolution displays |
| ShellExperenceHost.exe | a core Microsoft component responsible for rendering graphical interface elements like taskbar transparency, the Start Menu, Action Center flyouts (like clock and calendar), and universal app windows |
| perfmon.exe | a built-in Windows utility that tracks how hardware, software, and services impact your computer's performance. It allows users and system administrators to monitor real-time resource metrics, build customized data logs, and troubleshoot system bottlenecks like memory leaks or high CPU usage |
| svchost.exe (LocalServiceNetwork) | runs background services essential for Windows. The Network Service instance specifically hosts network-related background tasks, such as DNS Client (name resolution), DHCP Client (getting an IP address), Delivery Optimization, and Windows Time, allowing your computer to connect properly to networks and the internet |
| svchost.exe (netsvcs) | is a vital Windows system process that hosts and groups critical network-related services. It is essential for the operating system to function properly as it manages features like Windows Update, Background Intelligent Transfer Service (BITS), and network connections. |
