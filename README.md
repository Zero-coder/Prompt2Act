当然可以兄弟！下面是为你 **Prompt2Act** 项目撰写的一个完整的 `README.md` 草稿，适用于 GitHub 仓库的开源发布。内容包括项目简介、架构图、特性亮点、环境配置、快速上手、数据与模型下载、评估方式、BibTeX 引用等。

---

## 🧠 Prompt2Act: Mapping Prompts into Sequence of Robotic Actions with Large Foundation Models

> Official implementation of our system **Prompt2Act**, which maps open-ended multi-modal prompts into real-world robotic actions via large vision-language models, mixed execution agents, and visual grounding modules.

![system diagram](./figures/prompt2act_architecture.png)

---

### 🌟 Highlights

* **Multimodal Prompt Understanding**: Supports vision-language prompts such as images, sketches, pointing gestures, and free-form instructions.
* **Mixed Execution Agent**: Combines predefined symbolic functions and on-the-fly code generation to execute diverse tasks.
* **Visual Grounding via VG-Marker**: Automatically identifies objects and assigns semantic anchors from raw scenes using open-vocabulary segmentation + GPT-4o.
* **Supports Novel Tasks**: From "Arrange pens by reference photo" to "Pick the toy pointed by hand", with no finetuning needed.
* **Zero-shot generalization** to occluded, unseen, and cluttered environments.

---

### 📂 Project Structure

```
Prompt2Act/
│
├── prompt2act/                 # Core system modules
│   ├── planner/                # LLM-based sequence planner
│   ├── executor/               # Mixed Execution Agent (predefined + code-gen)
│   ├── visual_grounding/       # VG-Marker
│   └── utils/
│
├── data/                       # Demo trajectories & prompt configs
├── models/                     # LLM/VLM interface wrappers
├── scripts/                    # Evaluation scripts and launchers
└── README.md
```

---

### ⚙️ Installation

We recommend Python 3.10 and Linux/Ubuntu.

```bash
# Clone repository
git clone https://github.com/Zero-coder/Prompt2Act.git
cd Prompt2Act

# Create virtual env (optional)
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

---

### 🚀 Quick Start

Run a predefined task (e.g., *Arrange Pens by Reference*) in simulation:

```bash
python scripts/run_demo.py \
  --task arrange_pens \
  --prompt examples/prompts/arrange_pens.json
```

You can also modify the prompt file to test new tasks:

```json
{
  "instruction": "Please arrange these pens as shown in the image.",
  "image": "reference_pens.jpg"
}
```

---

### 🧠 Model & Assets

To fully enable Prompt2Act, you need:

* GPT-4o / GPT-4V (OpenAI API or local Azure proxy)
* SAM / Grounded-SAM for segmentation
* VG-Marker (included, no training needed)
* Predefined skills: `pick`, `place`, `rotate`, etc.

We provide starter checkpoints and test prompts in `/data`.

---

### 🧪 Evaluation

To evaluate Prompt2Act under different generalization axes:

```bash
python scripts/eval_benchmark.py \
  --benchmark occlusion \
  --config configs/eval_occlusion.yaml
```

You can test:

* Visual generalization (new textures, occlusion)
* Reasoning (visual constraints, sketch understanding)
* Embodiment shift (sim vs real)

---

### 📖 Citation

If you find this project helpful, please consider citing our paper:

```bibtex
@article{jiang2025prompt2act,
  title={Prompt2Act: Mapping Prompts into Sequence of Robotic Actions with Large Foundation Models},
  author={Maowei Jiang and Qi Wang and Hongfeng Ai and Zhiyong Dong and Yusong Hu and Ao Liang and Yifan Wang and Ruiqi Li and Quangao Liu and Moquan Chen and Peter Buš and Long Zeng},
  journal={Information Fusion},
  year={2025}
}
```

---

### 📬 Contact

Maintained by [@Zero-coder](https://github.com/Zero-coder).
Please open issues or pull requests for contributions.

---

如果你需要我再补充：

* demo 视频链接 / gif
* 环境依赖（例如需要的CUDA版本）
* 支持的硬件（myCobot、UR、etc.）

可以继续告诉我，我会帮你完善 README.md！

要我导出 Markdown 文件或直接打包 zip 也没问题\~
