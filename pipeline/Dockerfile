FROM python:3.13.11-slim

#Start to learn uv
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

WORKDIR /code 

COPY pyproject.toml .python-version uv.lock ./
COPY pipeline.py . 

#RUN pip install pandas pyarrow



#ENTRYPOINT ['python', 'pipeline.py']