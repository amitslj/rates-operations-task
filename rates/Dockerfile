# Docker File to run the Rates Frontend application
####STAGE 1: BUILD#####
FROM python
WORKDIR /app
COPY . /app
ENV NAME postgres
ENV USER postgres
ENV HOST rates_task_db
ENV PASSWORD pass123

####STAGE 2: RUN#####
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y python3-pip
RUN pip install -Ur requirements.txt
RUN pip install -U gunicorn
CMD [ "gunicorn", "-b", ":3000", "wsgi" ]