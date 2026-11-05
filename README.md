## Krishnapriya Rajeev

AI engineer at KeyValue Software Systems in Kochi. These days I work on LLM agents, mostly NL-to-SQL and RAG. I started out in computer vision.

[LinkedIn](https://www.linkedin.com/in/krishnapriya-r-27may2001) · [Email](mailto:krishofficial05@gmail.com)

### Skills

| | Now | Before |
|---|---|---|
| **Agents** | Agno, OpenAI Agents SDK, MCP | LangGraph |
| **Models** | Claude, Gemini, Vertex AI | OpenAI |
| **Methods** | NL-to-SQL, tool calling, structured output, LLM-as-judge evals | RAG, ReAct agents |
| **Vector&nbsp;search** | pgvector, sqlite-vec, hybrid search (RRF) | Qdrant |
| **Databases** | PostgreSQL, BigQuery, Redis, SQLite | Cloud SQL |
| **Backend** | Python, FastAPI, Pydantic, sqlglot, TypeScript, NestJS, GraphQL | |
| **Pipelines** | AWS SQS, Lambda | Dataflow (Apache Beam), Pub/Sub, asyncio, Playwright |
| **Speech** | Whisper, pyannote, voice cloning | |
| **Frontend** | React, Next.js, ECharts | Streamlit |
| **Vision** | | YOLO11, RF-DETR, ByteTrack, Depth Anything, MediaPipe, OpenCV |
| **Serving** | | TensorRT, ONNX, Triton, NVIDIA Jetson |
| **ML** | | PyTorch, scikit-learn, CatBoost, XGBoost, MLflow, Label Studio |
| **Cloud&nbsp;and&nbsp;CI** | GCP, AWS, Docker, GitHub Actions, pytest | SageMaker, EC2 |

### Work

- **NL-to-SQL analytics agent.** Answers plain-English questions with BigQuery SQL, charts and dashboards. I built the column-level access checks, the verified-query retrieval (hit@3 went from 0.83 to 0.98) and a 122-question eval set.
- **LLM shopping assistant** for a US retail-health company. A LangGraph agent with tools for price, inventory and cart. I also built its Dataflow and BigQuery pipelines for product data and logs.
- **Vehicle pose classifier.** YOLO11-pose plus geometry checks to tell which side of a car is in a photo. 99.5% correct on 735 test cars, trained through 3 SageMaker pipelines.
- **Legal document pipeline.** Collected 16.5M court judgments and laws to pretrain a small legal language model. asyncio, Playwright, S3.

### Projects

- [PitchMe](https://github.com/krishnapriyarajeev/pitchme): record a pitch, get feedback on voice, body language and content, then hear a better version in your own cloned voice. FastAPI, Whisper, pyannote, Expo.
- [Monocular Depth Estimation](https://github.com/krishnapriyarajeev/Monocular_Depth_Estimation): distance to each object from a single camera image, using YOLOv5 and MiDaS.

### Education

B.Tech in Computer Science, TKM College of Engineering, Kollam (2020 to 2024)
