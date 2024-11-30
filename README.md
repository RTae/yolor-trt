<div align="left">
    <img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="40%" align="left" style="margin-right: 15px"/>
    <div style="display: inline-block;">
        <h2 style="display: inline-block; vertical-align: middle; margin-top: 0;">YOLOR-TRT</h2>
        <p>
	<em>Empowering Vision with High-Speed Object Detection</em>
</p>
        <p>
	<img src="https://img.shields.io/github/license/RTae/yolor-trt?style=flat-square&logo=opensourceinitiative&logoColor=white&color=A931EC" alt="license">
	<img src="https://img.shields.io/github/last-commit/RTae/yolor-trt?style=flat-square&logo=git&logoColor=white&color=A931EC" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/RTae/yolor-trt?style=flat-square&color=A931EC" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/RTae/yolor-trt?style=flat-square&color=A931EC" alt="repo-language-count">
</p>
        <p>Built with the tools and technologies:</p>
        <p>
	<img src="https://img.shields.io/badge/Redis-DC382D.svg?style=flat-square&logo=Redis&logoColor=white" alt="Redis">
	<img src="https://img.shields.io/badge/RabbitMQ-FF6600.svg?style=flat-square&logo=RabbitMQ&logoColor=white" alt="RabbitMQ">
	<img src="https://img.shields.io/badge/Docker-2496ED.svg?style=flat-square&logo=Docker&logoColor=white" alt="Docker">
	<img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat-square&logo=Python&logoColor=white" alt="Python">
</p>
    </div>
</div>
<br clear="left"/>

<details><summary>Table of Contents</summary>

- [ Overview](#-overview)
- [ Features](#-features)
- [ Project Structure](#-project-structure)
  - [ Project Index](#-project-index)
- [ Getting Started](#-getting-started)
  - [ Prerequisites](#-prerequisites)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Testing](#-testing)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ License](#-license)
- [ Acknowledgments](#-acknowledgments)

</details>
<hr>

##  Overview

Yolor-trt is a pioneering open-source project providing an efficient, predictive personal protective equipment (PPE) detection system. This revolutionary technology leverages high-performance object detection models paired with convenient API endpoints, orchestrated services and asynchronous tasks handling. Designed for businesses, developers, and researchers, it ensures a safer workplace by accurately identifying PPE in visual content, delivering streamlined image processing, and facilitating rapid deployment.

---

##  Features

|      | Feature         | Summary       |
| :--- | :---:           | :---          |
| ⚙️  | **Architecture**  | <ul><li>Based on the combination of FastAPI, TensorRT and Celery for distributed PPE detection using image data sent via API calls.</li><li>Task queue and message brokering are managed by RabbitMQ and Redis, ensuring a robust, high-performance system.</li><li>TensorRT environment is prepared through a Dockerfile, ensuring smooth operation of the system.</li></ul> |
| 🔩 | **Code Quality**  | <ul><li>Consistent use of Python's PEP-8 conventions ensures code readability.</li><li>The code is clearly segmented into utilities, services, routes and controllers facilitating maintainability.</li><li>Use of Docker and docker-compose ensures consistent operation across different environments.</li></ul> |
| 📄 | **Documentation** | <ul><li>The primary language used in the project is Python, with the presence of yml, py, txt, and names file types.</li><li>Dependencies are managed by pip and can be found in `requirements.txt`.</li><li>Containers are defined using Docker and orchestrated using `docker-compose.yml`.</li></ul> |
| 🔌 | **Integrations**  | <ul><li>Integrated with TensorRT for efficient implementation of the deep learning model.</li><li>Utilizes FastAPI for routing and API endpoints management.</li><li>Deploys RabbitMQ and Redis for task queuing and message brokering respectively.</li></ul> |
| 🧩 | **Modularity**    | <ul><li>The project is modular with distinct directories for routes, services, controllers and utility functions.</li><li>Routes are managed by FastAPI routers, enhancing traceability and organization within the larger architectural framework.</li><li>Utility functions are abstracted out in `model_utils.py` for use across the application, encouraging code reusability.</li></ul> |
| 🧪 | **Testing**       | <ul><li>The project utilizes PyTest for running tests, as indicated by the test commands in the documentation.</li></ul> |
| ⚡️  | **Performance**   | <ul><li>The project leverages NVIDIA's TensorRT models for efficient model inference, contributing to faster results.</li><li>The use of Non-Maximum Suppression (NMS) in `model_utils.py` helps in predicting accurate output by eliminating redundant bounding boxes.</li></ul> |
| 🛡️ | **Security**      | <ul><li>Use of Docker containers, which provide added security through process isolation.</li></ul> |
| 📦 | **Dependencies**  | <ul><li>Managed by pip as defined in the `requirements.txt` file.</li><li>The system also relies on Docker, RabbitMQ, and Redis systems.</li></ul> |

---

##  Project Structure

```sh
└── yolor-trt/
    ├── PPEDetection
    │   ├── .gitignore
    │   ├── Dockerfile
    │   ├── main.py
    │   ├── requirements.txt
    │   └── src
    ├── README.md
    └── docker-compose.yml
```


###  Project Index
<details open>
	<summary><b><code>YOLOR-TRT/</code></b></summary>
	<details> <!-- __root__ Submodule -->
		<summary><b>__root__</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/docker-compose.yml'>docker-compose.yml</a></b></td>
				<td>- The docker-compose.yml orchestrates service creation for a predictive personal protective equipment (PPE) detection system, encompassing a main PPE detection service, an associated worker service, and two additional required services: Redis and RabbitMQ<br>- These coordinated services ensure efficient message brokering and task queuing for robust, high-performance PPE detection.</td>
			</tr>
			</table>
		</blockquote>
	</details>
	<details> <!-- PPEDetection Submodule -->
		<summary><b>PPEDetection</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/main.py'>main.py</a></b></td>
				<td>- MaineCoon is a FastAPI-based application outlined in PPEDetection/main.py, offering a comprehensive routing solution within the project structure through the integration of the API router<br>- It ensures smooth navigation and efficient functionality of various endpoints, contributing significantly to the architectural integrity of the entire codebase.</td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/requirements.txt'>requirements.txt</a></b></td>
				<td>- PPEDetection/requirements.txt lists the specific software dependencies required for the PPEDetection project<br>- It enables the setup of a uniform development environment and guarantees the smooth running of the project<br>- It includes packages necessary for computer vision tasks, web server operation, data serialization, and handling asynchronous tasks.</td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/Dockerfile'>Dockerfile</a></b></td>
				<td>- The Dockerfile in the PPEDetection directory sets up an environment for running a TensorRT-based application<br>- It begins with an Nvidia TensorRT base image, installs necessary Python packages, copies project requirements, and installs them<br>- Additionally, it updates system packages and installs utilities required for multimedia processing.</td>
			</tr>
			</table>
			<details>
				<summary><b>src</b></summary>
				<blockquote>
					<details>
						<summary><b>routes</b></summary>
						<blockquote>
							<table>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/routes/model_route.py'>model_route.py</a></b></td>
								<td>- Model_route.py forms part of the routing system in the PPEDetection application<br>- It handles image data sent via API calls for inference, initiates processing, and manages responses<br>- It also retrieves processing results once ready, converting them to a viewable image format for return to the client.</td>
							</tr>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/routes/routes.py'>routes.py</a></b></td>
								<td>- Routes.py in PPEDetection/src/routes acts as a connection point, integrating model_route with the APIRouter from FastAPI<br>- Predominantly, it assigns a specific "/model" prefix and "model" tag, enhancing the traceability and organization of the routes related to the model within the broader codebase architecture.</td>
							</tr>
							</table>
						</blockquote>
					</details>
					<details>
						<summary><b>controllers</b></summary>
						<blockquote>
							<table>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/controllers/model_controller.py'>model_controller.py</a></b></td>
								<td>- Model Controller in the PPEDetection project facilitates image inference tasks<br>- Leveraging helper functions, it converts image bytes to string format, then dispatches this data for further processing<br>- Thus, it serves as an important touchpoint for managing image parsing and initiating subsequent AI analysis tasks.</td>
							</tr>
							</table>
						</blockquote>
					</details>
					<details>
						<summary><b>queue</b></summary>
						<blockquote>
							<table>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/queue/worker.py'>worker.py</a></b></td>
								<td>- Worker.py configures and initializes the Celery application within the Personal Protective Equipment (PPE) Detection project<br>- It leverages environment variables for the broker and backend URI setups<br>- Additionally, it includes task definitions from the tasks file located within the same queue module, facilitating distributed task execution across worker nodes.</td>
							</tr>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/queue/tasks.py'>tasks.py</a></b></td>
								<td>- The 'tasks.py' within the PPEDetection/src/queue directory serves as the primary component for managing machine learning model prediction tasks<br>- It utilizes an abstraction of the Celery's Task class to efficiently load models for the first task call, eliminating the need to reload for each subsequent task<br>- It also provides an inference function for image data processing.</td>
							</tr>
							</table>
						</blockquote>
					</details>
					<details>
						<summary><b>utils</b></summary>
						<blockquote>
							<details>
								<summary><b>asserts</b></summary>
								<blockquote>
									<table>
									<tr>
										<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/utils/asserts/coco.names'>coco.names</a></b></td>
										<td>- The utility file 'coco.names' within the PPEDetection project serves as a predefined dictionary for object recognition<br>- It lists common objects from everyday items like 'bottle' or 'clock', to animals like 'dog', and transportation mediums like 'bicycle'<br>- It aids in identifying and labeling these objects within images or video frames for the personal protective equipment detection system.</td>
									</tr>
									</table>
								</blockquote>
							</details>
							<details>
								<summary><b>helper</b></summary>
								<blockquote>
									<table>
									<tr>
										<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/utils/helper/model_utils.py'>model_utils.py</a></b></td>
										<td>- The code in 'model_utils.py' provides various utility functions geared towards image processing and detection tasks<br>- Key functionalities include converting and resizing images, performing Non-Maximum Suppression (NMS) on prediction results, drawing bounding boxes for detection results, and handling image formats for further processing<br>- These functions support the primary tasks of the PPEDetection project.</td>
									</tr>
									</table>
								</blockquote>
							</details>
						</blockquote>
					</details>
					<details>
						<summary><b>services</b></summary>
						<blockquote>
							<table>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/services/trt_loader.py'>trt_loader.py</a></b></td>
								<td>- The 'trt_loader.py' file in the PPEDetection project is responsible for managing NVIDIA's TensorRT models<br>- It prepares, executes, and retrieves results from the inference engine<br>- Specifically, it handles memory allocation for the engine's inputs and outputs, performs inference, and manages the transfer of data between host and device<br>- Furthermore, it also reorganizes the model's flattened outputs back to their original shapes.</td>
							</tr>
							<tr>
								<td><b><a href='https://github.com/RTae/yolor-trt/blob/master/PPEDetection/src/services/model_service.py'>model_service.py</a></b></td>
								<td>- The code in 'model_service.py' is responsible for coordinating the entire object detection process<br>- It manages the loading and configuration of the YOLOR model, preprocesses images for detection, handles detection and results from the model, and conducts post-processing activities including drawing bounding boxes and scaling results back to original image size.</td>
							</tr>
							</table>
						</blockquote>
					</details>
				</blockquote>
			</details>
		</blockquote>
	</details>
</details>

---
##  Getting Started

###  Prerequisites

Before getting started with yolor-trt, ensure your runtime environment meets the following requirements:

- **Programming Language:** Python
- **Package Manager:** Pip
- **Container Runtime:** Docker


###  Installation

Install yolor-trt using one of the following methods:

**Build from source:**

1. Clone the yolor-trt repository:
```sh
❯ git clone https://github.com/RTae/yolor-trt
```

2. Navigate to the project directory:
```sh
❯ cd yolor-trt
```

3. Install the project dependencies:


**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ pip install -r PPEDetection/requirements.txt
```


**Using `docker`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```sh
❯ docker build -t RTae/yolor-trt .
```




###  Usage
Run yolor-trt using the following command:
**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ python {entrypoint}
```


**Using `docker`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```sh
❯ docker run -it {image_name}
```


###  Testing
Run the test suite using the following command:
**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ pytest
```


---
##  Project Roadmap

- [X] **`Task 1`**: <strike>Implement feature one.</strike>
- [ ] **`Task 2`**: Implement feature two.
- [ ] **`Task 3`**: Implement feature three.

---

##  Contributing

- **💬 [Join the Discussions](https://github.com/RTae/yolor-trt/discussions)**: Share your insights, provide feedback, or ask questions.
- **🐛 [Report Issues](https://github.com/RTae/yolor-trt/issues)**: Submit bugs found or log feature requests for the `yolor-trt` project.
- **💡 [Submit Pull Requests](https://github.com/RTae/yolor-trt/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/RTae/yolor-trt
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="left">
   <a href="https://github.com{/RTae/yolor-trt/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=RTae/yolor-trt">
   </a>
</p>
</details>

---

##  License

This project is protected under the [SELECT-A-LICENSE](https://choosealicense.com/licenses) License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

##  Acknowledgments

- List any resources, contributors, inspiration, etc. here.

---
