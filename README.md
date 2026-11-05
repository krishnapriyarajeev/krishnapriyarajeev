## Krishnapriya Rajeev

AI engineer at KeyValue Software Systems in Kochi. These days I work on LLM agents, mostly NL-to-SQL and RAG. I started out in computer vision.

[LinkedIn](https://www.linkedin.com/in/krishnapriya-r-27may2001) · [Email](mailto:krishofficial05@gmail.com)

### Now: LLM agents and backend

- **Agents:** LangGraph, Agno, OpenAI Agents SDK, MCP
- **Techniques:** NL-to-SQL, RAG, tool calling, structured output, LLM-as-judge evals
- **Vector search:** pgvector, Qdrant, sqlite-vec, hybrid search (RRF)
- **Databases:** PostgreSQL, BigQuery, Redis, SQLite
- **Backend:** Python, FastAPI, Pydantic, sqlglot, TypeScript, NestJS, GraphQL
- **Data pipelines:** Dataflow (Apache Beam), Pub/Sub, streaming and batch ETL, idempotent ingestion
- **Queues and workers:** AWS SQS, dead-letter queues, Lambda, asyncio, multiprocessing
- **Speech:** Whisper, pyannote, voice cloning
- **Cloud and CI:** GCP, Docker, GitHub Actions, pytest

### Before: computer vision and edge AI

- **Computer vision:** Ultralytics, RF-DETR, ByteTrack, Depth Anything, MediaPipe, OpenCV
- **Edge and serving:** NVIDIA Jetson, TensorRT, ONNX, Triton, GStreamer
- **ML:** PyTorch, scikit-learn, CatBoost, XGBoost, MLflow, Label Studio
- **AWS:** SageMaker Pipelines, EC2, S3, Kinesis Video Streams

### Work

- **NL-to-SQL analytics agent.** Answers plain-English business questions with BigQuery SQL, charts and dashboards that refresh daily. SQL checks block sensitive columns and cap query cost. Verified example queries guide the model (hit@3 went from 0.83 to 0.98), and evals grade the answers with an LLM judge.
- **LLM shopping assistant** for a US retail-health company. Shoppers ask about a product (details, reviews, coupons, store stock), compare it with others and add it to the cart. It runs on LangGraph workflows with RAG over reviews. Its logs stream through Pub/Sub and Dataflow into BigQuery and an analytics dashboard.
- **Vehicle pose classifier.** Checks that a car is at the right angle before a dealership photo is taken. A pose model finds the car, its 4 wheels and its view (99.5% correct on 735 validation cars), then geometry rules check the result. The model pre-labels new images in Label Studio, and 3 SageMaker pipelines handle data prep and training.
- **Legal document pipeline.** Collects Indian court judgments and laws as training data for a small legal language model. It found 16.5M document links and uses async workers, rate limiting, retries and resumable S3 uploads.

### Projects

- [PitchMe](https://github.com/krishnapriyarajeev/pitchme): record a pitch, get feedback on voice, body language and content, then hear a better version in your own cloned voice. FastAPI, Whisper, pyannote, Expo.
- [Monocular Depth Estimation](https://github.com/krishnapriyarajeev/Monocular_Depth_Estimation): distance to each object from a single camera image, using YOLOv5 and MiDaS.

### Education

B.Tech in Computer Science, TKM College of Engineering, Kollam (2020 to 2024)
