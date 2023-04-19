<!DOCTYPE html>
<html lang="en">
<body>
    <h1>Auto-Llama-cpp: An Autonomous Llama Experiment 🦙</h1>
    <p>...README content...</p>
<h2>Memory/Disk Requirements 💾</h2>
<p>As the models are currently fully loaded into memory, you will need adequate disk space to save them and sufficient RAM to load them. At the moment, memory and disk requirements are the same.</p>
<table>
    <tr>
        <th>Model</th>
        <th>Original Size</th>
        <th>Quantized Size (4-bit)</th>
    </tr>
    <tr>
        <td>7B</td>
        <td>13 GB</td>
        <td>3.9 GB</td>
    </tr>
    <tr>
        <td>13B</td>
        <td>24 GB</td>
        <td>7.8 GB</td>
    </tr>
    <tr>
        <td>30B</td>
        <td>60 GB</td>
        <td>19.5 GB</td>
    </tr>
    <tr>
        <td>65B</td>
        <td>120 GB</td>
        <td>38.5 GB</td>
    </tr>
</table>

<h2>Quick Tutorial 🚀</h2>
<p>Hi! I ended up trying this out recently and found a few issues but submitted a pull request for it. Here's a quick tutorial of what I did on how to get it up and running with my changes:</p>
<ol>
    <li>Run these commands:
        <pre><code>git clone https://github.com/rhohndorf/Auto-Llama-cpp.git
cd Auto-Llama-cpp
pip install -r requirements.txt</code></pre>
</li>
<li>Download <a href="https://huggingface.co/eachadea/legacy-ggml-vicuna-13b-4bit/resolve/main/ggml-vicuna-13b-4bit.bin">ggml-vicuna-13b-4bit.bin (8GB)</a> and place it in your models folder (for testing I made one in the root directory of this project with another folder called 13B for the size but if you're trying out multiple llms you'll likely have a folder somewhere else for all of them).</li>
<li>Rename "env.template" file to ".env" changing any environment variables that you need (like the path to your recently downloaded model).</li>
<li>Run this command to start:
<pre><code>python scripts/main.py</code></pre>
</li>
<li>Once you have things running and can see what it does, try changing ai_settings.yml and scripts/data/prompt.txt to change how the AI behaves.</li>
</ol>
## Acknowledgements and Credits 👏
This project is built on top of several open-source projects, and we would like to acknowledge and thank the original developers for their contributions to the AI and open-source community.

### Original Projects:
1. **Auto-GPT**: This project is a fork of Auto-GPT, which is an attempt to build an AI agent using GPT models that can interact with the user and perform tasks. Auto-GPT project can be found [here](https://github.com/rhohndorf/Auto-GPT).

2. **llama.cpp**: The project uses [llama.cpp](https://github.com/ggerganov/llama.cpp) under the hood for running the llama models locally. llama.cpp is an open-source project developed by [Georgi Gerganov](https://github.com/ggerganov).

3. **Open Assistant**: Auto-Llama-cpp plans to add support for [Open Assistant](https://github.com/LAION-AI/Open-Assistant) models, which is a project aiming to create an open-source AI assistant based on the GPT-3 architecture.

### Contributors:
- **[rhohndorf](https://github.com/rhohndorf)**: The creator of the Auto-Llama-cpp project and the main contributor.
- **[Georgi Gerganov](https://github.com/ggerganov)**: Developer of llama.cpp, which is used in this project for running the models locally.
- **[LAION-AI](https://github.com/LAION-AI)**: The team behind the Open Assistant project.

We encourage everyone to contribute to these projects and help improve the open-source AI ecosystem. If you have any suggestions, issues, or would like to contribute, feel free to submit a pull request or open an issue.

</body>
</html>