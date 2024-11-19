This source code allows a user to run an OpenAI Swarm agent connecting to multiple agents and functionality.

It offers these key features:

1. Creation of main agent
2. Creation of sub agents for multiple functions
3. Example of a RAG creation and retrieval
4. Example of a web search using Tavily
5. Example of a local calculate function
6. Example of a local config data request
7. Continuous user input until you exit

#################################
#Required Packages to download in console
##################################

pip install git+https://github.com/openai/swarm.git
pip install tavily-python
pip install llama-index llama-index-embeddings-fireworks
pip install docx2txt
pip install torch transformers python-pptx Pillow

##################################
# BUG RESOLUTION 
##################################
# At the current time, your IDE may show errors on the “Result” class because the Swarm source
# code on the Github repository has not registered this class in the initialization (I'm not sure why), 
# but you can easily add it to the __init__.py file in the root directory of the Swarm package:

from .core import Swarm
from .types import Agent, Response, Result
__all__ = ["Swarm", "Agent", "Response", "Result"]
