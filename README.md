## Krishnapriya Rajeev

AI engineer at KeyValue Software Systems in Kochi. These days I work on LLM agents, mostly NL-to-SQL and RAG. I started out in computer vision.

[LinkedIn](https://www.linkedin.com/in/krishnapriya-r-27may2001) · [Email](mailto:krishofficial05@gmail.com)

### Now: LLM agents and backend

- **Agents:** LangGraph, Agno, OpenAI Agents SDK, MCP
- **Techniques:** RAG, tool calling, structured output, guardrails, human-in-the-loop, LLM-as-judge evals
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
- **ML:** PyTorch, scikit-learn, MLflow, Label Studio
- **AWS:** SageMaker Pipelines, EC2, S3, Kinesis Video Streams

### Work

- **NL-to-SQL analytics agent.** Answers plain-English business questions with BigQuery SQL, charts and dashboards that refresh daily. SQL checks block sensitive columns and cap query cost. Verified example queries guide the model (hit@3 went from 0.83 to 0.98), and evals grade the answers with an LLM judge.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      a1["Question<br/>app or MCP"] --> a2["Agno agent<br/>writes SQL"]
      a3["Verified queries<br/>hybrid search"] --> a2
      a2 --> a4["Guardrails<br/>columns, cost"]
      a5["User approval<br/>big queries"] -.-> a4
      a4 --> a6["BigQuery<br/>chart, dashboard"]
  ```

  </details>

- **LLM shopping assistant** for a US retail-health company. Shoppers ask about a product (details, reviews, coupons, store stock), compare it with others and add it to the cart. It runs on LangGraph workflows with RAG over reviews. Its logs stream through Pub/Sub and Dataflow into BigQuery and an analytics dashboard.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      b1["Question on a<br/>product page"] --> b2["LangGraph agent<br/>intent, tools"]
      b2 --> b3["Price, stock,<br/>coupons, cart"]
      b2 --> b4["Review search<br/>RAG, Qdrant"]
      b2 --> b5["Compare table<br/>no LLM call"]
      b6["Product data"] --> b7["Gemini factors<br/>in Dataflow"] --> b5
      b2 -. logs .-> b8["Pub/Sub to<br/>Dataflow to<br/>BigQuery"]
  ```

  </details>

- **Vehicle pose classifier.** Checks that a car is at the right angle before a dealership photo is taken. A pose model finds the car, its 4 wheels and its view (99.5% correct on 735 validation cars), then geometry rules check the result. The model pre-labels new images in Label Studio, and 3 SageMaker pipelines handle data prep and training.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      v1["Label Studio<br/>model pre-labels"] --> v2["SageMaker<br/>3 pipelines"]
      v2 --> v3["Ultralytics pose<br/>view, 4 wheels"]
      v4["Camera frame"] --> v3
      v3 --> v5["Geometry rules<br/>right angle?"]
  ```

  </details>

- **Legal document pipeline.** Collects Indian court judgments and laws as training data for a small legal language model. It found 16.5M document links and uses async workers, rate limiting, retries and resumable S3 uploads.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      l1["Search pages<br/>split by date"] --> l2["Async harvest<br/>16.5M links"]
      l2 --> l3["Text download<br/>retries, resume"]
      l3 --> l4["S3<br/>JSON per doc"]
      l3 -.-> l5["Failure files<br/>for re-runs"]
  ```

  </details>

### Projects

- [PitchMe](https://github.com/krishnapriyarajeev/pitchme): practice a sales call with an AI buyer, then get a debrief on content, speech, voice and body language, with stronger answers played back in your own cloned voice. FastAPI, LiveKit, Whisper, pyannote, MediaPipe, Expo.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      p1["Deal setup<br/>buyer, stage"] --> p2["AI buyer call<br/>LiveKit, Groq"]
      p2 --> p3["Content<br/>LLM judge"]
      p2 --> p4["Speech<br/>Whisper"]
      p2 --> p5["Voice<br/>pitch, energy"]
      p2 --> p6["Body language<br/>MediaPipe"]
      p3 --> p7["Debrief<br/>scores, video"]
      p4 --> p7
      p5 --> p7
      p6 --> p7
      p3 --> p8["Better answers<br/>in your voice"]
  ```

  </details>

- [Monocular Depth Estimation](https://github.com/krishnapriyarajeev/Monocular_Depth_Estimation): distance to each object from a single camera image, using YOLOv5 and MiDaS.

  <details>
  <summary>Architecture</summary>

  ```mermaid
  flowchart LR
      m1["Video frame"] --> m2["YOLOv5 + SORT<br/>tracked objects"]
      m1 --> m3["MiDaS<br/>depth map"]
      m2 --> m4["Linear model<br/>depth to meters"]
      m3 --> m4
      m4 --> m5["Distance<br/>per object"]
  ```

  </details>

### Writing and teaching

- [TensorRT inference optimization on NVIDIA Jetson AGX Orin](https://www.keyvalue.systems/blog/from-bottlenecks-to-breakthroughs-how-tensorrt-video-analytics-revolutionized-our-pipeline/), KeyValue blog, co-written with Ratheesha S
- Talks and workshops at KeyValue on SQL agents, vector databases, image generation and Jetson
- Mentoring for new joiners in the fresher training program

### Education

B.Tech in Computer Science, TKM College of Engineering, Kollam (2020 to 2024)
