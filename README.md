# Oh Jaehong (오재홍) — Robotics / Control / Cognitive Robotics
I build robotic systems that **stay operational in the real world** and I research architectures where robots become **legible teammates** (not opaque tools).

**Links**
- Blog: https://jack0682.github.io/
- GitHub: https://github.com/jack0682
- Email: jaehongoh1554@gmail.com

<img width="2811" height="798" alt="image" src="https://github.com/user-attachments/assets/b9471351-dae5-4048-a0f6-fbf9f9c47aa2" />


---

## Focus (2026)
**Human-centered, safety-critical robotics under partial observability**
- Semantic perception → mapping → decision → **explainable action**
- **Topology-conditioned reasoning** (ONN / ORTSF)
- **Constraint-aware RL** for manipulation (Doosan M0609)

> Core thesis: **Robust autonomy = semantic continuity + safe decision-making + operational loops.**  
_Last updated: 2026-02-12 (KST)_

---

## What I can build (systems I actually implement)
### 1) Field-operational ROS2 autonomy (Nav2 reliability loop)
- Nav2 tuning for real environments (local/global planners, costmaps, recovery behaviors)
- Reproducible failure triage with **rosbag + logs** (issue isolation → fix → regression test)
- Real-time constraints mindset: latency budgets, QoS, callback scheduling

### 2) Safety monitoring pipeline (Perception → Event → Action → Dashboard)
- Detector/tracker pipeline for safety events (e.g., PPE / hazards)
- Event triggers → robot behavior (stop/alert/avoid) + logging
- Operator-facing monitoring via **MQTT → WebSocket → Web UI**

### 3) Explainable & structured decision representations
- Scene-graph / ontology-ready state representations
- Topology/constraint framing for stability and reasoning (ONN / ORTSF)
- “Why did the robot do that?” → human-readable rationales

---

## Research: Papers (arXiv)
### Ontology Neural Network (ONN) / ORTSF
- **Ontology Neural Networks for Topologically Conditioned Constraint Satisfaction** — arXiv:2601.05304 (2026)  
  https://arxiv.org/abs/2601.05304
- **Constructive Lyapunov Functions via Topology-Preserving Neural Networks** — arXiv:2510.24730 (2025)  
  https://arxiv.org/abs/2510.24730
- **Ontology Neural Network and ORTSF: A Framework for Topological Reasoning and Delay-Robust Control** — arXiv:2506.19277 (2025)  
  https://arxiv.org/abs/2506.19277

### Cognitive Synergy Architecture (CSA)
- **Cognitive Synergy Architecture: SEGO for Human-Centric Collaborative Robots** — arXiv:2506.13149 (2025)  
  https://arxiv.org/abs/2506.13149
- **Towards Cognitive Collaborative Robots: Semantic-Level Integration and Explainable Control for Human-Centric Cooperation** — arXiv:2505.03815 (2025)  
  https://arxiv.org/abs/2505.03815

### Robotics Manipulation / RL
- **Learning to Assemble the Soma Cube with Legal-Action Masked DQN and Safe ZYZ Regrasp on a Doosan M0609** — arXiv:2508.21272 (2025)  
  https://arxiv.org/abs/2508.21272

---

## Featured projects (code & systems)
### 1) CSA (Cognitive Synergy Architecture) — system-level cognitive robotics
- Repo: **CSAv1** — https://github.com/jack0682/CSAv1  
- Keywords: semantic mapping, scene graph, explainable control, HRI-ready interfaces

### 2) ONN (Ontology Neural Network) — topology-conditioned reasoning + constraint satisfaction
- Repo: **ONN** — https://github.com/jack0682/ONN  
- Anchored by: ONN/ORTSF papers above

### 3) Robot Web Dashboard (MQTT → WebSocket → Web UI)
- Repo: **web_robot_interface** — https://github.com/jack0682/web_robot_interface  
- Purpose: command-center style monitoring (ROS2 Robot → MQTT Broker → WebSocket Bridge → Web Dashboard)

### 4) 3D / Projection utilities (perception pipelines)
- Repo: **Projection_plane** — https://github.com/jack0682/Projection_plane

### 5) Line tracking / navigation experiments
- Repo: **linetracking** — https://github.com/jack0682/linetracking

---

## Technical stack

<img width="2752" height="1536" alt="image" src="https://github.com/user-attachments/assets/7775d00a-c56b-4437-a89e-3f1b3f210a23" />

### Robotics & Autonomy
- **ROS2 (Humble)**, Nav2, TF2, URDF, RViz  
- rosbag-based debugging, QoS tuning, callback groups / executors
- Multi-robot topic/namespace design, message/service/action contract design

### Perception / Mapping
- RGB-D pipelines (depth → 3D points → map-frame transform)
- Detection / tracking integration (YOLO + tracking stack), event extraction
- SLAM / mapping: ORB-SLAM2, RTAB-Map  
- Point cloud ops: PCL, registration/filters (typical: voxel, crop, plane/cluster)

### Control / RL / Safety
- Classical control: PID, feedforward+feedback, state-space intuition
- RL: DQN variants / PPO usage patterns, **action masking**, safety guards
- Manipulation safety: constraint design, singularity-aware motion constraints (Doosan M0609 context)

### Backend / Ops / Monitoring
- **MQTT** (robot telemetry + events), WebSocket streaming
- FastAPI-style backend patterns, structured logging, config-driven systems (YAML/JSON)
- Telemetry storage patterns (time-series mindset; reproducible logs)

### Programming / Tooling
- Python (primary), C/C++, MATLAB  
- Git, Linux (Ubuntu), Docker/venv, CI-friendly repo structuring
- Data formats: JSON/CSV/JSONL; scene-graph export (Neo4j-ready structuring)

---

## If you’re a lab / recruiter
I’m interested in:
- **human–robot teaming** in safety-critical environments
- **occlusion / partial observability** + risk-aware planning
- **explainable policies** that can be audited in the field

Best contact: **jaehongoh1554@gmail.com**
