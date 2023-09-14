FROM python

WORKDIR /app

EXPOSE 5050

COPY Pipfile Pipfile.lock ./

RUN pip install pipenv
RUN pipenv requirements > requirements.txt
RUN pip install -r requirements.txt
RUN pip install --upgrade Flask Jinja2
RUN pip install --upgrade Jinja2


COPY . ./

CMD ["python","main.py"]

