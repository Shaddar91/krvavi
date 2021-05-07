FROM shaddar/flask:v1

WORKDIR /var/www/app
COPY . /var/www/app/
RUN chmod +x /var/www/app/bin/activate
ENV VIRTUAL_ENV=$(pwd)
RUN python3 -m virtualenv --python=python3 ${VIRTUAL_ENV}
ENV PATH="$VIRTUAL_ENV/bin:$PATH"
RUN pip3 install -r requirements.txt
CMD flask run --host='0.0.0.0'