FROM ubuntu
RUN apt-get update ; apt-get -y install fortune
ADD app.sh /bin/app.sh
RUN chmod +x /bin/app.sh
ENTRYPOINT ["/bin/app.sh"]
CMD ["10"]
# CMD is passing argument to app.sh, which is the interval in seconds