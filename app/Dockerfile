FROM python:3.12-slim-bookworm
COPY ./requirements.txt /app/requirements.txt
WORKDIR /app
RUN pip install -r requirements.txt
RUN mkdir -p /app/log
COPY app.py /app
EXPOSE 5000
CMD ["python", "app.py" ]

# Для Grafana
#FROM grafana/grafana
#COPY grafana-defaults.ini grafana.ini /etc/grafana/
#COPY *.json /grafana/dashboards/
#ENTRYPOINT ["/usr/sbin/grafana-server", "--homepath=/usr/share/grafana", "--config=/etc/grafana/grafana.ini"]
