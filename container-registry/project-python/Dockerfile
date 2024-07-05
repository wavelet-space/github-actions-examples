FROM python:3-alpine

WORKDIR /usr/src/app

COPY main.py  ./
COPY pyproject.toml ./

RUN pip install --no-cache-dir .

CMD ["project-python"]
