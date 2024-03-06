# Get base image with python 3.9
# -------------------- Stage1-----------------------------
FROM python:3.9 AS backend-builder 

RUN apt-get update -y 
# Copy the source code to the workdir in container

COPY ./ /app

# Your Working directory

WORKDIR /app

# Install all requirements dependencies with backend builder base
RUN pip install -r requirements.txt
Run pip install flask
#-------------------Stage2------------------------------

FROM python:3.9-slim

WORKDIR /app

COPY --from=backend-builder /usr/local/lib/python3.9/site-packages/ /usr/local/lib/python3.9/site-packages/

COPY --from=backend-builder /app /app

CMD [ "python","run.py" ]
