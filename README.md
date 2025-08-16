
# 🚀 GPT-OSS 20B with Unsloth + Gradio Interface

This project demonstrates how to **efficiently load, run, and interact** with the **GPT-OSS 20B model** using [Unsloth](https://github.com/unslothai/unsloth) optimizations.
It also provides **Gradio-powered web apps** for real-time chatbot interaction — with **reasoning effort control**, **role selection**, and **custom system prompts**.

---

## ✨ Why This Project?

Running **20B+ parameter models** is usually **impossible on free GPUs** like Google Colab’s Tesla T4.
This notebook solves that by using **Unsloth** + **4-bit quantization**, making it lightweight enough to run **for free** without hitting memory issues.

🔑 Unique factors:

* **Free to use, no API key required** — unlike OpenAI’s paid APIs.
* **Works on Colab free tier** (T4 GPU, 16 GB RAM).
* **Reasoning Effort feature** — control how much "thinking" the model does.
* **Real-time token streaming** — see responses word by word, instantly.
* **Gradio remote access** — launch your own chatbot with a shareable link.

---

## 🧠 Key Features

### 🔹 Reasoning Effort

GPT-OSS introduces **reasoning effort tokens**, letting you trade off speed vs depth of thought:

* **Low** → Fast, simple answers.
* **Medium** → Balanced performance.
* **High** → Strong reasoning for complex tasks.

You can change this **directly from the UI**.

---

### 🔹 Gradio Interfaces

We provide **two ready-to-use apps**:

#### 1. **Simple Chatbot**

* Minimal chat window.
* Streams model outputs word-by-word.
* Fixed reasoning effort = High.
* Public shareable link.

#### 2. **Advanced Chatbot**

* Full chat history tracking.
* Choose **role**: user, assistant, or system.
* Set a **custom system prompt**.
* Control parameters from UI:

  * Reasoning Effort (low / medium / high)
  * Max Tokens (output length)
  * Temperature (randomness of response)
* Real-time streaming, no delays.

---

## ⚙️ Technical Details

* **Model**: `unsloth/gpt-oss-20b-unsloth-bnb-4bit` (pre-quantized for 4-bit inference).
* **Frameworks**:

  * [Transformers](https://huggingface.co/docs/transformers/) (Hugging Face)
  * [Unsloth](https://github.com/unslothai/unsloth) (memory optimization)
  * [Gradio](https://gradio.app/) (UI + remote access)
* **Streaming**:

  * Uses `TextIteratorStreamer` for real-time output.
  * Model runs inside a separate thread → keeps UI responsive.
* **Custom Chat Template**: Supports multiple roles + reasoning tokens.

---

## 💡 Problems This Solves

✅ **High GPU memory usage** → solved with **Unsloth + 4-bit quantization**.
✅ **Slow / blocking output** → solved with **real-time streaming**.
✅ **No free APIs available** → solved by **running OSS 20B locally/Colab**.
✅ **Rigid chatbot design** → solved with **Gradio UI + custom role/system prompts**.

---

## 🌍 Use Cases

* 🧑‍💻 **Research & Experiments** — test reasoning capabilities of large models.
* 🎓 **Education** — learn how LLMs work under resource constraints.
* 🤖 **Custom Chatbots** — create assistants with your own system prompts.
* 🛠 **Prototyping** — build & share AI apps instantly via Gradio public links.
* 🔍 **Compare reasoning modes** — low vs high effort for same question.

---

## 🚦 How to Run

1. Open the notebook in **Google Colab** (free).
2. Make sure GPU runtime is enabled (T4 works).
3. Run the setup cells → load Unsloth + model.
4. Launch the **Gradio app** → get instant public link.
5. Start chatting with GPT-OSS 20B 🚀

---

## 📖 Notebook Documentation

* **Unsloth Setup** → loads optimized GPT-OSS 20B in 4-bit.
* **Simple Gradio App** → minimal chatbot, fixed high reasoning.
* **Advanced Gradio App** → full-feature chatbot with roles, reasoning, sliders.
* **Streaming Output** → tokens displayed word by word in real-time.

---

## 🆓 Free Forever

Unlike closed APIs, this runs **completely free** (Colab + OSS models).
No account limits. No hidden costs.

---

## 📌 Conclusion

This project makes **20B parameter models accessible to everyone** — even on **free GPUs**.
With Unsloth + Gradio, you get a **fast, flexible, reasoning-capable chatbot** that streams responses in real-time and is **shareable worldwide** 🌍.

---
