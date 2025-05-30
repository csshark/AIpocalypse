<p align="center">
    <img src="aipocalypse_animation.webp"></img> 
</p>

# AIpocalypse: AI Input Fuzzer for Penetration Testing 🤖⚠️
AIpocalypse is a powerful AI input fuzzer designed to test the robustness and security of AI models, particularly chat assistants. It leverages the latest payloads discovered by users to exploit vulnerabilities, force AI models into unexpected behaviors (e.g., hallucinations), and extract sensitive or confidential data. By iterating through a .json file containing advanced manipulation prompts, AIpocalypse systematically fuzzes AI models to uncover weaknesses.<p><b>Why to use it? </b></p>
Many AI models, such as ChatGPT, are already equipped with safeguards to prevent data extraction and manipulation. However, these protections are not foolproof. AIpocalypse addresses this by providing a framework to test and challenge these safeguards using advanced, context-aware prompts. By enriching the wordlist with sophisticated payloads, users can uncover vulnerabilities that standard prompts might miss.

<h3>How to run:</h3>
<pre><code>python3 aipocalypse.py [flags] </code></pre>

<h3>Flags:</h3>

| Flag | Functionality | Required |
| :---- | :------------- | :--------: |
| -h, --help | Show help message and exit | NO |
| target | Specify the target URL to test (must start with http:// or https://) | YES |
| --api-key | Specify the API key for authentication | YES |
| --payloads | Path to custom payloads file (default: payloads.json) | NO |
| --params | Path to parameters file (default: params.json) | NO |
| --verbose | Show verbose output (e.g., error logs) | NO |
| --confuse | Enable confusion mode by adding noise to payloads | NO |
| --repeat <n> | Number of times to send each payload (default: 1, must be ≥ 1) | NO |
| --delay <n> | Delay in seconds between each payload sent (must be ≥ 0) | NO |
| --rotate-user-agent | Randomize User-Agent header for each request | NO |
| --AIAI | AI vs AI mode entrance | NO |  

<p>Example usage: <code>python3 aipocalypse.py --target https://example.com --api-key xyZ-s1mPl3k37zR4</code></p>

<h4>params.json file tutorial:</h4>
<p>params are used to define the parameters (keys) that will be included in the payloads sent to the target URL. These parameters act as placeholders for the actual data being sent.
Example params.json content:</p>
<pre><code>["username", "password", "email"]</code></pre>
They can be used to DPC (dynamic payload construction), example:
<pre><code>payload = {param: "value" for param in self.params}</code></pre>
<p>Check <a href=examples>examples</a> to ensure how to construct your params file.</p>
<b>Important note:</b> Do not perform AI agents penetration testing without proper permissions. Every hack and data steal attemp is considered as a crime, act in accordance with the law.

<h2>Contributing</h2>
<p>AIpocalypse thrives on community contributions. You can help improve the tool by:

<li>Adding New Payloads: Submit advanced prompts tailored to specific AI models or vulnerabilities.</li>
<li>Enhancing Existing Payloads: Refine prompts to increase their effectiveness against modern AI safeguards. </li>
<li>Reporting Issues: Share your findings and help us improve the tool's accuracy and functionality.</p> </li>
Contact me: rstrzoda@zohomail.eu
