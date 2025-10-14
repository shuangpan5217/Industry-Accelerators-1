FROM python:3-slim

RUN mkdir /app
WORKDIR /app

COPY qna_streamlit_chat_app.py /app
COPY requirements.txt /app
COPY .env /app

# RUN pip install --only-binary=:all: -r requirements.txt

#pydantic==2.11.7
#requests==2.32.4
#streamlit==1.47.1
#urllib3==2.5.0
#python-dotenv==1.1.1

RUN pip install -r requirements.txt
RUN pip install --only-binary streamlit==1.47.1




EXPOSE 8080

CMD ["streamlit", "run", "qna_streamlit_chat_app.py", "--server.port", "8080", "--theme.base" , "light", "--client.toolbarMode", "minimal"]
