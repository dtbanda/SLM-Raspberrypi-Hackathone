# 🧠 Lightweight AI for Rural Africa

An offline, containerised Small Language Model (SLM) built to run on low-cost edge devices like the Raspberry Pi — bringing the power of AI to rural environments without needing internet connectivity.

## 🌍 Why This Project?

Many people in rural areas of Africa — including teachers, nurses, and engineers — often lack stable internet access to use modern tools like search engines or online AI models. This project provides a solution by running a lightweight language model locally on a Raspberry Pi 3B, making intelligent assistance completely accessible offline.

## 🚀 Features

- 🧠 Fully offline small language model (SLM) from [Liquid AI](https://huggingface.co/LiquidAI)
- 🐍 FastAPI-powered REST API interface with browser access
- 📦 Docker containerization for portable deployment
- 💡 Designed for edge use cases in education, healthcare, and engineering
- 🌐 Accessible over LAN — no internet required

---

## ⚙️ Raspberry Pi Specs (Tested)

| Component         | Specification                        |
|------------------|--------------------------------------|
| Model             | Raspberry Pi 3B                      |
| CPU               | Quad-Core ARM Cortex-A53 1.2GHz     |
| RAM               | 1 GB LPDDR2                         |
| Storage           | 16 GB microSD card (Class 10)        |
| OS                | Raspberry Pi OS Lite (64-bit)        |
| Network           | Ethernet or WiFi                     |

---

## 📦 Getting Started

You can run this app locally on any ARM64-compatible Linux machine (including Raspberry Pi 3/4) using Docker.

### 🔄 Option 1: Pull Prebuilt Image (Recommended for Raspberry Pi)

```bash
docker pull dtbanda/slm-pi-app:arm64
docker run -dp 8000:8000 dtbanda/slm-pi-app:arm64
```
### 🛠 Option 2: Build Image Locally (for custom changes or processor compatibility eg x86)

```
git clone https://github.com/dtbanda/SLM-Raspberrypi-Hackathone.git
cd SLM-Raspberrypi-Hackathone
docker build -t local-slm-ai .
docker run -dp 8000:8000 local-slm-ai
````
## 🌐 Accessing the Assistant

Once the container is running:

Open your browser and go to: `http://localhost:8000`

Or, from another device on the same network: `http://<IP-of-device-running-app>`

You can also test the API using the interactive Swagger UI at:
`http://localhost:8000/docs`

------
## 📚 Use Cases

- Teachers accessing lesson material offline

- Nurses retrieving dosage or medical info without internet

- Engineers troubleshooting equipment with local AI prompts

- NGOs deploying tools in disconnected environments

-------
## 🔬 Under the Hood

- Model: Liquid AI 350M SLM via Hugging Face

- Framework: FastAPI + Uvicorn

- Container: Docker (ARM64 compatible)

- Frontend: Basic HTML interface or Swagger UI

- Inference: Local execution on Raspberry Pi
-----
## 🛣 Potential Future Roadmap
- 🔡 Vernacular language support (Bemba, Swahili, Nyanja)

- 📚 Custom fine-tuning for educational and health datasets

- 📦 Offline deployment kits for rural schools and clinics
------  
## 🤝 Contributing
We welcome ideas, translations, or performance improvements. If you're interested in contributing to expanding AI access across Africa and other disconnected regions, feel free to fork, suggest features, or reach out.

## 📄 License
MIT License — see LICENSE for details.
-----
## 🙏 Acknowledgements
- Liquid AI for open-source SLMs

- FastAPI and Docker communities

- Feedback from teachers, nurses, and engineers in Zambia

## Demo Video Link[https://www.youtube.com/watch?v=R7EHec47lE4&ab_channel=DalitsoBanda]

## 📣 Author
### Dalitso Banda
**Cloud Engineer | Infrastructure for AI | DevOps |**


