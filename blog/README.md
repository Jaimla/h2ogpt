# Building the World's Best Open-Source Large Language Model: H2O.ai's Journey

by Arno Candel, PhD, CTO H2O.ai, April 19 2023

At H2O.ai, we pride ourselves on developing world-class Machine Learning, Deep Learning, and AI platforms.
In the rapidly growing field of AI, Large Language Models (LLMs) have proven their immense potential in various applications such as natural language processing, code completion, reasoning, mathematics, and more.

We are proud to announce that we are building h2oGPT, an LLM that not only excels in performance but is also fully open-source and commercially usable, providing a valuable resource for developers, researchers, and organizations worldwide.

In this blog, we'll explore our journey in building h2oGPT in our effort to democratize AI.

## Why Open-Source LLMs?

While LLMs like OpenAI's ChatGPT/GPT-4, Microsoft's Bing AI Chat, Google's Bard, and Cohere are powerful and effective, they have certain limitations compared to open-source LLMs:

1. **Data Privacy and Security**: Using hosted LLMs requires sending data to external servers. This can raise concerns about data privacy, security, and compliance, especially for sensitive information or industries with strict regulations.
2. **Dependency and Customization**: Hosted LLMs often limit the extent of customization and control, as users rely on the service provider's infrastructure and predefined models. Open-source LLMs allow users to tailor the models to their specific needs, deploy on their own infrastructure, and even modify the underlying code.
3. **Cost and Scalability**: Hosted LLMs usually come with usage fees, which can increase significantly with large-scale applications. Open-source LLMs can be more cost-effective, as users can scale the models on their own infrastructure without incurring additional costs from the service provider.
4. **Access and Availability**: Hosted LLMs may be subject to downtime or limited availability, affecting users' access to the models. Open-source LLMs can be deployed on-premises or on private clouds, ensuring uninterrupted access and reducing reliance on external providers.

Overall, open-source LLMs offer greater flexibility, control, and cost-effectiveness, while addressing data privacy and security concerns. They foster a competitive landscape in the AI industry and empower users to innovate and customize models to suit their specific needs.

## Why h2oGPT?

Existing open-source LLMs have several limitations:

1. **License Restrictions**: Some models like Llama carry non-permissive (e.g., GPL) licenses that disallow commercial use. Other models like Dolly were trained on data with copy-left licences that prevents fine-tuning without open-sourcing.
2. **Not Ready for Use**: Models like Pythia or GPT-NeoX are likely undertrained and/or not fine-tuned for downstream tasks like code completion or chatbots.
3. **Too small or too big**: Models like Bloom are either too small (<=7B parameters) or too big (176B parameters), also likely undertrained, and not ready for business use.
4. **Fine-tuned on questionable data at best**: Models like Alpaca, GPT4All are trained on data that was collected from ChatGPT (e.g. via ShareGPT), and their terms of service disallow competitive use.

We aimed to create a powerful LLM using fully permissive data and models, enabling broader access for businesses and commercial products without legal concerns, thus expanding access to cutting-edge AI while adhering to licensing requirements.

## The H2O.ai LLM Ecosystem

Our open-source LLM ecosystem currently includes the following components:

1. **Code, data, and models**: We provide a fully permissive, commercially usable open-source repository that includes code, data, and models.
2. **Fine-tuning**: Our ecosystem features code for preparing large open-source datasets for fine-tuning, including prompt engineering, making it easy to fine-tune LLMs up to 20 billion parameters (hopefully more soon) on commodity hardware and enterprise GPU servers.
3. **Chatbot**: We offer code to run a chatbot on GPU servers, with a shareable end-point and Python client API, allowing you to evaluate and compare the performance of fine-tuned LLMs.
4. **H2O LLM Studio**: Our no-code LLM fine-tuning framework makes it even easier to work with our models.

## Roadmap and Future Plans

We have an ambitious roadmap for our LLM ecosystem, including:

1. Integration with downstream applications and low/no-code platforms
2. Complementing our chatbot with search and other APIs
3. High-performance distributed training of larger models on trillion tokens
4. Improvements in code completion, reasoning, mathematics, factual correctness, hallucinations, and reducing repetitions

## Getting Started with H2O.ai's LLM

To start using our LLM, follow the steps below:

1. Clone the repository: `git clone https://github.com/h2oai/h2ogpt.git`
2. Change to the repository directory: `cd h2ogpt`
3. Install the requirements: `pip install -r requirements.txt`
4. Run the chatbot: `python generate.py --base_model=h2oai/h2ogpt-oig-oasst1-256-6.9b`
5. Open your browser at `http://0.0.0.0:7860` or the public live URL printed by the server.

For more information, visit [H2O.ai's Hugging Face page](https://huggingface.co/h2oai) and [H2O LLM Studio](https://github.com/h2oai/h2o-llmstudio) GitHub repository.

Join us on this exciting journey as we continue to improve and expand the capabilities of our open-source LLM ecosystem!
