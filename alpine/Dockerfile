FROM alpine
RUN apk --no-cache add curl bash
RUN echo 'export PS1="[\u@\h] \w \$ "' >> /root/.bashrc
ENTRYPOINT ["bash"]
