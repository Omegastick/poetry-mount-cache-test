FROM python:3.9

RUN pip install poetry

WORKDIR /app
COPY ./ /app
RUN --mount=type=cache,target=/root/.cache/pypoetry,id=test-poetry \
    poetry config installer.max-workers 10 && poetry install --no-root
# RUN --mount=type=cache,target=/root/.cache/pip,id=test-pip \
#     pip install -r requirements.txt