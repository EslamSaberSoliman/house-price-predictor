FROM python:3.9-slim

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt --retries 5 --timeout 120 && export STREAMLIT_SERVER_FILE_WATCHER_TYPE=none


EXPOSE 8501

CMD ["streamlit", "run", "app.py", "--server.address=0.0.0.0" ]