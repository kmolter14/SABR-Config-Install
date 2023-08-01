# SABR-Config-Install
Welcome to the SABR-Config-Install repository. This comprehensive guide provides detailed instructions for hardware assembly and software installation, allowing you to efficiently set up and optimize your SABR box.

Hardware Components
Here is a detailed list of all the hardware components you will need (https://www.amazon.com/hz/wishlist/ls/3M4DD1A7FHZYL?ref_=wl_share):

3M 4026 Natural Polyurethane Double Coated Foam Tape, 0.75" width x 5yd length (1 roll)

SAMSUNG Electronics 870 EVO 2TB 2.5 Inch SATA III Internal SSD (MZ-77E2T0B/AM)

NETGEAR 8-Port Gigabit Ethernet Unmanaged Switch (GS308) - Home Network Hub, Office Ethernet Splitter, Plug-and-Play, Silent Operation, Desktop or Wall Mount

Libre Computer Board ROC-RK3328-CC (Renegade) Mini Computer with Gigabit Ethernet and USB 3.0 (4GB)

LK COKOINO Raspberry Pi Pico Starter Kit with Pre-Soldered Header, 830 Points Solderless Breadboard, 65pcs Jumper Cables, Raspberry Pi Pico Case and Screwdriver

XHF 3/4" Strong Back-Glue Self Adhesive Black Cable Zip Tie Mounts 100pcs with 8" Zip Ties, Screws, UV Protection Outdoor Sticky Wire Fasteners Cable Clips Management Anchors Organizer Holders Squares

SOULWIT Cable Holder Clips, 5 Pack Self Adhesive Cord Organizer for Home/Office/Desk/Car/Phone/USB Cable Wire Management (for Cables Less Than 5mm) - Black

Geekworm for Raspberry Pi 3 B+ Case, Aluminum Alloy Heavy Duty Passive Cooling Metal Case with Heatsink Pillar Compatible with Raspberry Pi 3 Model B+/Raspberry Pi 3 Model B-Black (P252)

GL.iNet GL-AXT1800 (Slate AX) Pocket-Sized Wi-Fi 6 Gigabit Travel Router, Extender/Repeater for Hotel&Public Network, VPN Client&Server, OpenWrt, Adguard Home, USB 3.0, Network Storage, TF Card Slot

Noctua NF-F12 iPPC 3000 PWM, Heavy Duty Cooling Fan, 4-Pin, 3000 RPM (120mm, Black) for Desktop

HOTNOW Micro USB Cable 1ft 3Pack, 12inch Short Android Charger Cable Nylon Braided Fast Charging Cord for Samsung Galaxy S7 S6 S7 Edge S5,Note 5,PS4,Power Bank and More

SmartQ H302S USB 3.0 Hub for Laptop with 2ft Long Cable, Multi Port Expander, Fast Data Transfer USB Splitter Compatible with Windows PC, Mac, Printer, Mobile HDD

CRJ Full Speed 12V Voltage Step-Up USB to 3-Pin and 4-Pin PC Fan Sleeved Power Adapter Cable

IBL-Single Gang Wall Plate with Brush Bristles (Black)

Cat 6 Ethernet Cable 1.5ft (6 Pack) (at a Cat5e Price but Higher Bandwidth) Flat Internet Network Cable - Cat6 Ethernet Patch Cable Short - Black Cat6 Computer Cable with Snagless RJ45 Connectors

Noctua NA-FC1, 4-Pin PWM Fan Controller (Black)

FANCYWING 500X500X1.5MM 2.0MM 2.5MM 3.0MM 3.5MM 4.0MM 5.0MM 6.0MM Carbon Fiber Sheet 100% 3K Carbon Fiber Laminate Plate Matt Surface Twill Weave Panel Sheet 4.0MM Thickness(Matte Finish)

Beelink Mini PC, AMD Ryzen 5 5500U(6C/12T, Up to 4.0GHz), 16GB DDR4 RAM 500GB NVMe SSD, SER5 Win 11 Mini Desktop Computer Support 4K@60Hz Output/WiFi6/BT5.2/DP1.4/HDMI2.0/USB3.2 for Gaming/Office/Home

UCTRONICS Male to Female GPIO Ribbon Cable 40pin 8inch Breadboard Jumper Wires for Connection Raspberry Pi 3 2 Model B B+ w/ 3.5/5 inch TFT Touch Screen LCD Display

Milwaukee 48-22-8450 PACKOUT Tool Case with Foam Customizable Insert

Power Strip with USB C, 4 Widely Spaced Outlets and 4 USB Ports 5 FT Extension Cord, BEVA Surge Protector Power Strip Mountable USB Power Strip 1250W/10A for Smartphone Tablets, Home, Travel, Office

GELRHONR 4.9Ft 90 Degrees 3 Prong AC to IEC320 C5 Power Cord,18AWG 100V~250V Up Angle NEMA 5-15P to Left Angle 3-Slot Mickey Mouse Universal Power Cable for Notebook Computers, TV, Monitors

UGREEN SATA to USB 3.0 Adapter Cable for 2.5" SSD and HDD Hard Drive Adapter 5Gbps Support SATA III UASP Compatible with Samsung Seagate WD Hitachi Toshiba PS3 PS4 Xbox PC Router 1.5FT

Hardware Build Instructions
Here are step-by-step instructions to build your SABR system:

Assemble the Raspberry Pi: Begin by placing the Raspberry Pi into the Geekworm case, secure the Pi in place with the provided screws. Attach the Noctua fan to the case using the provided screws or adhesive pads. Connect the fan to the GPIO pins on the Raspberry Pi for power.

Prepare the Storage: Connect the Samsung EVO SSD to your computer using the UGREEN SATA to USB Adapter. Format and partition the SSD according to your preferred Operating System.

Set up the Network Switch: Connect the Ethernet ports of the Raspberry Pi and the Beelink Mini PC to the NETGEAR Gigabit Ethernet Switch.

Prepare the Power Supply: Connect all your components that need power to the Power Strip.

Connect the Router: Connect the GL.iNet GL-AXT1800 router to the switch. You'll want to put the router in bridge mode, as the Mini PC will act as your main router.

Final Assembly: Organize all components in the Milwaukee PACKOUT Tool Case, and manage the cables with the self-adhesive cord holders and cable ties. The IBL-Single Gang Wall Plate with Brush Bristles can be used to create a neat cable entry/exit point in the case.

Final Check: Connect the power strip to an AC power source and verify that all components power on correctly.

Please note: The specific assembly may vary depending on your specific use case and additional components. Always ensure all components are powered off before making or changing connections.

Software Applications
Here is a list of the software applications you will need:

Dashy
Docker
PiHole
Storage NPM
Dev NPM
Mattermost
Wiki
Filebrowser
Portainer
Gitlab
Jupyter Labs
Home Assistant

Software Installation Instructions
Follow these instructions to install each software application on your SABR system:

Dashy: Start by cloning the Dashy repository on your machine using git clone https://github.com/Lissy93/dashy.git. Navigate to the cloned folder with cd dashy and run yarn install to install the required dependencies. Finally, start the application using yarn start.

Docker: To install Docker, you can use the convenience script provided by Docker. Simply run curl -fsSL https://get.docker.com -o get-docker.sh to download the script, and then sudo sh get-docker.sh to run it. After installing Docker, ensure to add your user to the Docker group by running sudo usermod -aG docker your-user.

PiHole: To install PiHole, you can use the automated install script by running curl -sSL https://install.pi-hole.net | bash.

Storage NPM and Dev NPM: To install these, simply run npm install storage and npm install dev respectively.

Mattermost: Mattermost provides an easy-to-use Docker deployment method. Simply run docker run --name mattermost-preview -d --publish 8065:8065 mattermost/mattermost-preview to download and run the Mattermost server.

Wiki: Install Wiki.js by running docker run -d -p 8080:80 requarks/wiki:2.

Filebrowser: To install Filebrowser, you can use Docker by running docker run -v /path/to/your/files:/srv -p 80:80 filebrowser/filebrowser.

Portainer: Install Portainer using Docker with docker volume create portainer_data followed by docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce.

Gitlab: To install Gitlab, use the Omnibus package server by adding the Gitlab repository with curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh | sudo bash, then install with sudo EXTERNAL_URL="http://gitlab.example.com" apt-get install gitlab-ee.

Jupyter Labs: Install Jupyter Labs by running pip install jupyterlab.

Home Assistant: Install Home Assistant using Docker with docker run --init -d --name="home-assistant" -e "TZ=America/New_York" -v /path/to/your/config:/config -p 8123:8123 homeassistant/home-assistant:stable.

Please ensure Docker and NPM are installed correctly before attempting to install Docker and NPM based applications. Always follow software-specific documentation for the most detailed and up-to-date installation instructions.
