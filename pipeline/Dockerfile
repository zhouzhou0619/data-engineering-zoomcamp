FROM python:3.13.11-slim

#Start to learn uv
COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/

WORKDIR /code 

COPY pyproject.toml .python-version uv.lock ./

#RUN pip install pandas pyarrow
#install dependencies
RUN uv sync --locked

COPY pipeline.py . 

ENTRYPOINT ["uv", "run", "python", "pipeline.py"]