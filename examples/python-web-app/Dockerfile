FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv && \
    python3 -m venv /app/venv && \
    /app/venv/bin/pip install -r requirements.txt
    cd devops
ENV PIP_BREAK_SYSTEM_PACKAGES 1

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




