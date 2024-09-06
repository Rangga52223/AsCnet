<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">AsCnet</h3>

  <p align="center">
    Simple IDS with Ai Detection
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

Introducing AsCnet, a simple yet powerful Intrusion Detection System (IDS) developed in Python. Leveraging the capabilities of Machine Learning and Deep Learning, AsCnet efficiently scans networks to detect potential threats. Created as a college side project, this open-source solution is designed to be user-friendly while providing advanced network security features. Explore the potential of AsCnet and experience the ease of detecting network threats with cutting-edge technology.

Why did you choose this:
* easy configuration
* easy to run
* Works automatically to detect attacks via computer networks

that's why you chose this tool, disclaimer this tool uses datasets to train its AI, if you want to help increase the performance of this tool, you can contribute to developing this tool, and also this tool is still under development and active, currently it is still detecting DDOS , in the future we will add several detections such as web exploitation and infiltration. Thank You


<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- GETTING STARTED -->
## Getting Started

To run this tool you can choose only one server or one server with an agent, so this tool is running using Pyshark to run the scanner and send it to the agent to be processed and get the detection results.

### Prerequisites

Before running the tool, you must install the requirements
* linux
  ```sh
  sudo python3 requirements.py
  ```
* Windows
  ```sh
  python requirements.py
  ```
Disclaimer: installing Wireshark on the server device is absolutely necessary to use Pyshark

### Installation

_Entering the installation stage, the steps are not too complicated, just follow them._

#install all requirements, on the agent and server
#### Agent
1.  Extract Zip

2.  edit settings.yaml with text editor
* yaml
  ```sh
  server:
    host: "192.168.0.101"
    port: 8000
  logging:
    log_file: "network_log.csv"
    log_level: "INFO"
  ```
  change host with your agent ip and port you like, for log_file change with your name file you like.

3.  running the agent
* bash/cmd
  ```sh
  python agent.py
  ```
  Next to Server
#### Server
The server in this tool is a tool for scanning networks so this is an important part even though it is second only to the agent.
1.  edit config.yaml with your text editor
* yaml
  ```sh
  websocket_host: "127.0.0.1"
  websocket_port: 8000
  network_interface: "Wi-Fi"
  excluded_ports:
    - 8000
  ```
for the host, replace it with the host agent's IP and it must be the same as the host agent's IP, for the port it must also be the same as the agent, for network_interface, replace it with which interface you want to scan, for exclude_port: for which port you don't want to scan.
2.  Running Server with sudo
* bash/cmd
  ```sh
  sudo python3 server.py
  ```
If there are problems when running, usually because there are firewall restrictions, you can set the firewall to block ports.
</br>
Disclaimer: This tool is still in early development so there are several features that are not yet available
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

If the tool runs successfully a log will appear in the agent.


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Machine Learning Scanning
- [x] Up github
- [ ] Deep Learning Scanning
- [ ] Add Visualitation with web
- [ ] simple Saver log
- [ ] All Attack Server Scanner
- [ ] Multi-language Support
    - [x] English
    - [x] Indonesian
    - [ ] Melayu
    - [ ] Japanese

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contribute and Report bugs 

I am very happy that there are people who want to help with this tool and help with bug reports. If you want to contribute to this tool, you can use the Google form link provided, thank you.
<br>
If you contribute to the attack dataset the form will be different, include the source link of the dataset you got, if you created the dataset you can just include your name/username, thank you
<br>
Contribute and bug reports link : Coming soon
Dataset Contribute link : Coming soon

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@R4n99aN](https://x.com/R4n99aN) - rangga52223@gmail.com

Project Link: [[AsCnet](https://github.com/Rangga52223/AsCnet)]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/rangga-wahyu-nugroho-869352224/
[product-screenshot]: images/screenshot.png
