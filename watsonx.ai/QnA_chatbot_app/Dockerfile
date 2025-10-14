FROM python:3-slim

# Install build tools and other dependencies required for CMake
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    cmake \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir /app
WORKDIR /app

COPY qna_streamlit_chat_app.py /app
COPY requirements.txt /app
COPY .env /app

RUN pip install -r requirements.txt

EXPOSE 8080

CMD ["streamlit", "run", "qna_streamlit_chat_app.py", "--server.port", "8080", "--theme.base" , "light", "--client.toolbarMode", "minimal"]
