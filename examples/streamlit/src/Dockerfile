FROM public.ecr.aws/lambda/python:3.12
COPY --from=public.ecr.aws/awsguru/aws-lambda-adapter:0.7.0 /lambda-adapter /opt/extensions/lambda-adapter

WORKDIR /app

COPY app.py requirements.txt ./
RUN python -m pip install -r requirements.txt

ENTRYPOINT [ "streamlit", "run", "app.py" ]