***
#### by Pradeep Devananth - [DoYourDuty.github.io](https://doyourduty.github.io/blogs.html)
## 1) **Amazon Bedrock** – the GenAI platform (models, RAG, agents, guardrails)

*   **What it is:** Managed platform to build GenAI apps and **agents** at production scale; single API to 100+ FMs (incl. **Amazon Nova**, Anthropic Claude, Meta, Mistral, etc.). [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)
*   **Key sub‑features (high level):**
    *   **AgentCore** (agentic runtime to build/deploy/operate agents) + **Agents for Bedrock** (guided agent builder) [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/), [\[itpro.com\]](https://www.itpro.com/technology/artificial-intelligence/aws-goes-all-in-on-ai-agents-with-new-features-for-bedrock-and-amazon-q)
    *   **Knowledge Bases** (managed **RAG**, now **multimodal retrieval** across text/images/audio/video) [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html), [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/multimodal-retrieval-bedrock-knowledge-bases/)
    *   **Guardrails** (policy layer for safety, PII redaction, topic filters; usable with models/agents/KB/flows) [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-how.html), [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-use.html)
    *   **Converse / Streaming APIs** (uniform chat/inference) and model choice including **Amazon Nova** tiers (Micro/Lite/Pro, etc.) [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/), [\[preporato.com\]](https://preporato.com/certifications/amazon/generative-ai-developer-professional/articles/amazon-bedrock-complete-guide-aip-c01-exam-2026)
*   **Typical uses:** Secure enterprise chat, RAG assistants, workflow agents, multimodal search/answers, tool‑calling agents. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/), [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
*   **Integrations:**
    *   **API/SDK:** `InvokeModel`, **Converse/ConverseStream**; tool‑use and function calling via Agents/AgentCore. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-use.html), [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)
    *   **UI:** Bedrock console playgrounds for models/agents/KB/guardrails. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)
    *   **MCP:** via **AgentCore gateway** and services (e.g., Amazon Connect MCP tools) to wire standardized tools into agents. [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/amazon-connect-mcp-support/)
    *   **Other AWS:** S3 (data), **OpenSearch Serverless** vectors, Lambda, API Gateway, CloudWatch; plug into Step Functions/Events for orchestration. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)

***

## 2) **Amazon Nova (model family on Bedrock)** – AWS first‑party LLMs

*   **What it is:** Amazon’s own FM family optimized for cost/latency/reasoning/multimodal; multiple tiers (**Micro/Lite/Pro**, etc.). [\[preporato.com\]](https://preporato.com/certifications/amazon/generative-ai-developer-professional/articles/amazon-bedrock-complete-guide-aip-c01-exam-2026)
*   **Use:** Chat/agents, multimodal understanding, fast/cheap inference. Select tier per task. [\[preporato.com\]](https://preporato.com/certifications/amazon/generative-ai-developer-professional/articles/amazon-bedrock-complete-guide-aip-c01-exam-2026)
*   **Integration:** Same Bedrock **Converse API** and Agents/AgentCore. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)

***

## 3) **Amazon Titan (Bedrock)** – embeddings & generation models

*   **What it is:** AWS enterprise‑focused FMs (not open‑weights). Current docs highlight **Text Embeddings v2**, **Multimodal Embeddings**, **Image Generator G1 v2**. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/titan-models.html)
*   **Use:** High‑quality embeddings for RAG, image generation, multimodal indexing. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/titan-models.html)
*   **Integration:** Use in **Knowledge Bases** (embeddings), Bedrock APIs; pair with OpenSearch/Pinecone. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)

***

## 4) **Amazon Q (suite of assistants)**

### a) **Amazon Q Business / Amazon Quick Suite (evolution)**

*   **What it is:** Enterprise AI assistant for **search, insights & actions** across your data; now positioned as/alongside **Amazon Quick Suite**—a unified, agentic workspace for research, BI, and automation (evolution of QuickSight + Q Business). [\[aws.amazon.com\]](https://aws.amazon.com/q/business/), [\[jkevinxu.github.io\]](https://jkevinxu.github.io/github-blog/2025/10/20/amazon-quick-suite-vs-amazon-q.html), [\[community.ibm.com\]](https://community.ibm.com/community/user/blogs/diptanu-roy/2025/10/10/amazon-quick-suite)
*   **Features:** Unified search across 40+ systems, citations, **Q Apps** (lightweight AI apps), actions in SaaS like Jira/Salesforce, and integration with office tools. [\[aws.amazon.com\]](https://aws.amazon.com/q/business/)
*   **Integrations:**
    *   **UI:** Web app, Slack, Outlook/Word/Teams add‑ins. [\[aws.amazon.com\]](https://aws.amazon.com/q/business/)
    *   **API/Connectors:** Built‑in connectors; reuse **Q Index** with Quick Suite. [\[aws.amazon.com\]](https://aws.amazon.com/q/business/)
    *   **MCP:** Ecosystem momentum and AWS tooling moving toward MCP support (see Q Developer CLI note). [\[awsinsider.net\]](https://awsinsider.net/articles/2025/04/03/aws-embraces-model-context-protocol-for-agentic-ai-development.aspx)

### b) **Amazon Q Developer**

*   **What it is:** Dev assistant in IDE/CLI/AWS Console with **autonomous agents** for code, tests, upgrades, cloud ops. Successor to CodeWhisperer. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/), [\[cloudvisor.co\]](https://cloudvisor.co/amazon-q/)
*   **Recent adds:** Conversation persistence/search, repo context controls, broader language support, code transformation agents. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/)
*   **Integrations:**
    *   **IDE/CLI/UI:** VS Code, JetBrains, AWS Console; **CLI**. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/)
    *   **MCP:** AWS pre‑announced MCP support for **Q Developer CLI** and shipped MCP servers to bring AWS best‑practices into assistants. [\[awsinsider.net\]](https://awsinsider.net/articles/2025/04/03/aws-embraces-model-context-protocol-for-agentic-ai-development.aspx)

***

## 5) **AWS “Frontier Agents” for SDLC** – Kiro / Security / DevOps

*   **What they are:** A newer class of **autonomous** agents that can run for hours/days on goal‑driven tasks—**Kiro** (autonomous coding), **AWS Security Agent**, **AWS DevOps Agent**. [\[aboutamazon.com\]](https://www.aboutamazon.com/news/aws/amazon-ai-frontier-agents-autonomous-kiro), [\[aboutamazon.com\]](https://www.aboutamazon.com/news/aws/aws-re-invent-2025-ai-news-updates)
*   **AWS DevOps Agent (preview):** Autonomously triages incidents, correlates observability + code + deploys, suggests remediations; integrations with CloudWatch, Datadog, Dynatrace, New Relic, Splunk, GitHub/GitLab; **MCP server integration supported**. [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/)
*   **Kiro & Security Agent:** Long‑running code work, multi‑repo changes; security reviews/pen‑tests guidance across SDLC. [\[theregister.com\]](https://www.theregister.com/2025/12/02/aws_kiro_devops_coding_agents/), [\[techcrunch.com\]](https://techcrunch.com/2025/12/02/amazon-previews-3-ai-agents-including-kiro-that-can-code-on-its-own-for-days/)
*   **Integrations:**
    *   **UI:** IDE & web UIs (Kiro in dev envs). [\[theregister.com\]](https://www.theregister.com/2025/12/02/aws_kiro_devops_coding_agents/)
    *   **APIs/Toolchain:** Hooks into CI/CD, repos, observability; **MCP** extensibility (DevOps Agent). [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/)

***

## 6) **Amazon SageMaker (for custom GenAI)**

*   **What it is:** Managed ML platform; for GenAI you’ll mostly touch **JumpStart** (deploy open/proprietary FMs), fine‑tuning, distributed training, evals, and optimized inference. [\[aws.amazon.com\]](https://aws.amazon.com/sagemaker/ai/jumpstart/), [\[pages.awscloud.com\]](https://pages.awscloud.com/rs/112-TZM-766/images/AWS_GenAI_on_Amazon_SageMaker.pdf)
*   **Use:** When you need **own model control** (fine‑tune OSS FMs, custom training), high‑throughput inference, or advanced MLOps. [\[github.com\]](https://github.com/aws-samples/amazon-sagemaker-generativeai)
*   **Integrations:**
    *   **API/SDK:** SageMaker SDK/endpoints; can front with API Gateway/Lambda. [\[aws.amazon.com\]](https://aws.amazon.com/sagemaker/ai/jumpstart/)
    *   **UI:** SageMaker Studio/Canvas (no‑code), JumpStart console. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/training-and-certification/building-ml-excellence-a-practical-training-guide-for-amazon-sagemaker-ai/), [\[aws.amazon.com\]](https://aws.amazon.com/sagemaker/ai/jumpstart/)

***

## 7) **AWS App Studio** – GenAI‑powered **low‑code app builder**

*   **What it is:** Natural‑language to **multi‑page enterprise app** (UI, data model, business logic). GA since late 2024. [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/), [\[siliconangle.com\]](https://siliconangle.com/2024/11/18/aws-app-studio-launches-general-availability-making-everyone-app-builder/)
*   **Use:** Rapidly build internal apps; can add GenAI features and integrate data sources. [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/)
*   **Integrations:**
    *   **UI:** Visual builder; describe changes in NL. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/aws/build-custom-business-applications-without-cloud-expertise-using-aws-app-studio-preview/)
    *   **Connectors/APIs:** AWS & SaaS connectors; publish app with role‑based access. [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/)

***

## 8) **PartyRock** – Bedrock **playground** (no‑code GenAI apps)

*   **What it is:** Browser playground to create/share GenAI mini‑apps; free daily usage tier announced. [\[partyrock.aws\]](https://partyrock.aws/), [\[aws.amazon.com\]](https://aws.amazon.com/blogs/aws/introducing-new-partyrock-capabilities-and-free-daily-usage/)
*   **Use:** Fast prototyping, demos, learning; remixable app blocks. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/publicsector/build-your-first-ai-assistant-with-partyrock/)
*   **Integration:** Web UI; powered by Bedrock behind the scenes (export ideas to real apps later). [\[partyrock.aws\]](https://partyrock.aws/)

***

## 9) **MCP (Model Context Protocol) on AWS** – standardizing tool access for agents

*   **Where it shows up:**
    *   **Amazon Connect** now supports **MCP tools** so AI agents can call standardized functions during customer interactions (look up orders, refunds, etc.). [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/amazon-connect-mcp-support/)
    *   **AWS DevOps Agent** supports connecting to your **own MCP server** for extra tools; AWS also published guidance to **deploy MCP servers on AWS**. [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/), [\[github.com\]](https://github.com/aws-solutions-library-samples/guidance-for-deploying-model-context-protocol-servers-on-aws/blob/main/README.md)
    *   **Q Developer CLI:** AWS announced incoming MCP support and MCP servers for code assistants. [\[awsinsider.net\]](https://awsinsider.net/articles/2025/04/03/aws-embraces-model-context-protocol-for-agentic-ai-development.aspx)
*   **Why it matters:** Easier cross‑tool integrations for **agents** without bespoke connectors. [\[marktechpost.com\]](https://www.marktechpost.com/2025/07/20/model-context-protocol-mcp-for-enterprises-secure-integration-with-aws-azure-and-google-cloud-2025-update/)

***

# Integration cheat‑sheet (how to connect things quickly)

| Goal                                      | Fastest path                                            | Notes                                                                                                                                                                                                                                                                                                                        |
| ----------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **App uses LLM chat/RAG**                 | **Bedrock** (Converse API + **Knowledge Bases**)        | Add **Guardrails**. Store data in S3; vectors in OpenSearch Serverless via KB. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html), [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/guardrails-use.html)                       |
| **Agent that calls tools/APIs**           | **Bedrock AgentCore / Agents**                          | Define tools (Lambda/APIs); optionally expose tools via **MCP** for broader reuse. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/), [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/amazon-connect-mcp-support/)                                                      |
| **Enterprise “ask‑my‑company” assistant** | **Amazon Q Business / Quick Suite**                     | Point to data sources; build **Q Apps** for actions; surface via web/Slack/Office. [\[aws.amazon.com\]](https://aws.amazon.com/q/business/)                                                                                                                                                       |
| **Developer productivity**                | **Amazon Q Developer** (+ frontier agents if available) | IDE/CLI help, code upgrades, repo‑wide changes; watch MCP updates. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/), [\[awsinsider.net\]](https://awsinsider.net/articles/2025/04/03/aws-embraces-model-context-protocol-for-agentic-ai-development.aspx) |
| **Ops/SRE incident handling**             | **AWS DevOps Agent**                                    | Hooks into CloudWatch/Datadog/etc.; extend via **MCP** to custom tools. [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/)                                                                                                                                                                |
| **Custom model training/fine‑tune**       | **SageMaker (+ JumpStart)**                             | Fine‑tune/open‑weights, deploy endpoints; use API Gateway for app integration. [\[aws.amazon.com\]](https://aws.amazon.com/sagemaker/ai/jumpstart/)                                                                                                                                               |
| **Low‑code internal app**                 | **AWS App Studio**                                      | NL‑describe → app; add GenAI features; RBAC and connectors baked‑in. [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/)                                                                                                                                                                      |
| **Prototype in minutes**                  | **PartyRock**                                           | Share link; later harden in Bedrock/App Studio. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/aws/introducing-new-partyrock-capabilities-and-free-daily-usage/)                                                                                                                               |

***

## Example integration patterns (API / UI / MCP)

*   **API**:
    *   Frontend → **API Gateway** → **Lambda** → **Bedrock Converse** (optionally call **KB** / **Agents**) → respond. Add **CloudWatch** logs & metrics. [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
*   **UI**:
    *   Business users: **Q Business/Quick Suite** web app, Slack/Outlook add‑ins. Developers: **Q Developer** in IDE/CLI. Builders: **Bedrock console** and **App Studio**. [\[aws.amazon.com\]](https://aws.amazon.com/q/business/), [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/), [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/)
*   **MCP**:
    *   Run an **MCP server** (on ECS/Lambda per AWS guidance) that exposes your internal APIs (ERP/ITSM). Point **DevOps Agent**, **Q Developer**, or **Connect** agents to it. [\[github.com\]](https://github.com/aws-solutions-library-samples/guidance-for-deploying-model-context-protocol-servers-on-aws/blob/main/README.md), [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/), [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/amazon-connect-mcp-support/)

***

## TL;DR by your list (and what to add)

*   **Bedrock** ✅ platform for models/agents/RAG/guardrails. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)
*   **Bedrock AgentCore** ✅ agent runtime. [\[aws.amazon.com\]](https://aws.amazon.com/bedrock/)
*   **SageMaker** ✅ for training/fine‑tune/open models (via **JumpStart**). [\[aws.amazon.com\]](https://aws.amazon.com/sagemaker/ai/jumpstart/)
*   **Amazon Q / Q Developer** ✅ developer + business assistants; Quick Suite evolution on the business side. [\[aws.amazon.com\]](https://aws.amazon.com/blogs/devops/april-2025-amazon-q-developer/), [\[aws.amazon.com\]](https://aws.amazon.com/q/business/)
*   **AWS DevOps Agent** ✅ frontier agent for incidents. **Also consider Kiro & Security Agent** for coding/security. [\[aws.amazon.com\]](https://aws.amazon.com/devops-agent/), [\[aboutamazon.com\]](https://www.aboutamazon.com/news/aws/amazon-ai-frontier-agents-autonomous-kiro)
*   **Add**: **Amazon Nova** (AWS LLMs), **Amazon Titan** (embeddings/image), **App Studio** (low‑code GenAI apps), **PartyRock** (playground), and **MCP integrations** across Connect/Agents/DevOps/Q. [\[preporato.com\]](https://preporato.com/certifications/amazon/generative-ai-developer-professional/articles/amazon-bedrock-complete-guide-aip-c01-exam-2026), [\[docs.aws.amazon.com\]](https://docs.aws.amazon.com/bedrock/latest/userguide/titan-models.html), [\[aws.amazon.com\]](https://aws.amazon.com/appstudio/), [\[partyrock.aws\]](https://partyrock.aws/), [\[aws.amazon.com\]](https://aws.amazon.com/about-aws/whats-new/2025/11/amazon-connect-mcp-support/)

***
