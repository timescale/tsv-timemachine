# Welcome to the Timescale Vector Time Machine
Chat with the git history of any git repo.
- Built with OpenAI, LlamaIndex, Streamlit and Timescale Vector.
- TSV Time Machine is an example of time aware retrieval augmented generation. Time aware retrieval involves RAG with a retrieval step that searches for vectors that are semantically most similar to a user query and that also fall within a specified time range.
- TSV Time Machine enables you to go back in time and chat with the commit history of any GitHub repository. Each Git commit entry has a timestamp associated with it, as well as a natural language message and other metadata (e.g author, commit, hash etc).

See a live demo of the app [here](https://pg-timemachine.streamlit.app/).
- The demo is pre-loaded with the history from PostgreSQL. The demo disables loading data from other git repos. To load data, launch your own fork.

## Get a free PostgreSQL vector database to use with this app
Spin up a [free cloud PostgreSQL database](https://console.cloud.timescale.com/signup?utm_campaign=vectorlaunch&utm_source=github&utm_medium=direct) with Timescale Vector to use in this sample app. You'll get 90 days free by signing up with the link above.

## Launching a fork.
To load data and try the demo on any other git repo, simply:
1) Fork the repo 
2) Launch your own streamlit app. 
3) Set the following [streamlit secrets](https://docs.streamlit.io/streamlit-community-cloud/deploy-your-app/secrets-management): 
    - `OPENAI_API_KEY` - Your openAI key.
    - `TIMESCALE_SERVICE_URL` - Your Timescale Service URL. Sign up for an account [here](https://www.timescale.com/ai).
    - `ENABLE_LOAD=1` - Enables Loading Data
