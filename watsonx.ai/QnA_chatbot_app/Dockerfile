FROM python:3-slim

RUN mkdir /app
WORKDIR /app

COPY qna_streamlit_chat_app.py /app
COPY requirements.txt /app
COPY .env /app

# RUN pip install --only-binary=:all: -r requirements.txt
RUN pip install --only-binary <package_name1>,<package_name2> <package_name1> <package_name2>

EXPOSE 8080

CMD ["streamlit", "run", "qna_streamlit_chat_app.py", "--server.port", "8080", "--theme.base" , "light", "--client.toolbarMode", "minimal"]
