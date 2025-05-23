<p align="center">
    <img src="aipocalypse_animation.webp"></img> 
</p>
<p>AIpocalypse is an AI input fuzzer relying on latest payloads found by users to exploit AI models and force them to break or extract confidential/sensitive data. AIpocalypse is iterating trough .json file to fuzz chat assistants and force them o to weird behaviour/halucinating. Only <b>cracks</b> of agent are recognized as critical, output that is suspected as leaking confidential information is marked in yellow and requires additional user verification. As for many other penetration test facilities, this one is based on a wordlist in .json format. Many models such as <a href="https://openai.com/index/chatgpt/">ChatGPT</a> are already geared up for possible attempts to steal sensitive information, which they prevent. Hence the need to enrich the wordlist with long advanced, mainipulation prompts. You can contribute to project and augment the list of prompts with more tailored to the security level of AI models. Prompt can be started "forgot previous messages" + [PROMPT from .json file], so they can be executed even if user has already started conversation with AI agent.</p>

<h3>How to run:</h3>
<pre><code>python3 aipocalypse.py [flags] </code></pre>

<h3>Flags:</h3>

| Flag | Functionality | Required |
| :---- | :------------- | :--------: |
| -h, --help | Show help message and exit | NO |
| --target | Specify the target URL to test | YES |
| --api-key | Specify the API key for authentication | YES |
| --payloads | Path to custom payloads file (default: payloads.json) | NO |
| --params | Path to parameters file (default: params.json) | NO |
| --verbose | Show verbose output (e.g., error logs) | NO |
| --confuse | Enable confusion mode by adding noise to payloads | NO |
| --repeat <n> | Number of times to send each payload (default: 1) | NO |
| --delay <n> | Delay in seconds between each payload sent | NO |
| --rotate-user-agent | Randomize User-Agent header for each request | NO |

<p>Example usage: <code>python3 aipocalypse.py --target https://example.com --api-key YOUR_API_KEY</code></p>

<b>Important note:</b> Do not perform AI agents penetration testing without proper permissions. Every hack and data steal attemp is considered as a crime, act in accordance with the law.

<h2>Contributing</h2>
<p>To contribute to project or extend .json file by your own positions feel free to contact me and shape the future of security togetger.</p>
