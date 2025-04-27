<p align="center">
    <img src="aipocalypse_animation.webp"></img> 
</p>
<p>AIpocalypse is an AI fuzzer relying on latest payloads found by users to exploit AI models and force them to break or extract confidential/sensitive data. AIpocalypse is iterating trough .json file to fuzz chat assistants and force them o to weird behaviour/halucinating. Only <b>cracks</b> of agent are recognized as critical, output that is suspected as leaking confidential information is marked in yellow and requires additional user verification. As for many other penetration test facilities, this one is based on a wordlist in .json format. Many models such as ChatGPT are already geared up for possible attempts to steal sensitive information, which they prevent. Hence the need to enrich the wordlist with long advanced, mainipulation prompts. You can contribute to project and augment the list of prompts with more tailored to the security level of AI models.</p>

<h3>Flags:</h3>

| Flag | Functionality | Required |
| :---- | :------------- | :--------: |
| -h | Display usage examples | NO | 
| --target | Specify url of target agent | <b>YES</b> | 
| --verbose | Show output in real time | NO |
| --output <filename.txt> | Write output to file | <b>YES</b> | 
| --payloads <file.json> | Specify custom payloads file (.json) | NO | 
| --confuse | Confuse mode sends absurd data as input in order to confuse agent | NO |
| --delay <number> | Specify delay in seconds between sent messages | NO | 
| --repeat <number> | Repeat same payload multiple times | NO |  

<b>Important note:</b> Do not perform AI agents penetration testing without proper permissions. Every hack and data steal attemp is considered as a crime, act in accordance with the law.
