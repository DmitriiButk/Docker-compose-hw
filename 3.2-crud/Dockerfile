FROM python

WORKDIR /app

RUN pip install --upgrade pip

COPY ./requirements.txt .

RUN pip install -r requirements.txt

COPY ./stocks_products .

COPY ./entrypoint.sh .

ENTRYPOINT ["sh", "entrypoint.sh"]




