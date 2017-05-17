FROM python:2.7.13-alpine

# support for https
# https://github.com/google/cadvisor/issues/1131#issuecomment-257382321
RUN apk add --update openssl; \
  # itchat can be installed with this little one-line command
  # https://github.com/littlecodersh/ItChat
  pip install itchat; \

  mkdir robot; \

  cd robot; \

  # tuling plugin can be get here:
  # https://github.com/littlecodersh/EasierLife/tree/master/Plugins/Tuling
  wget https://raw.githubusercontent.com/littlecodersh/EasierLife/master/Plugins/Tuling/tuling.py \
    https://raw.githubusercontent.com/littlecodersh/EasierLife/master/Plugins/Tuling/tuling.json

# https://docs.docker.com/engine/reference/builder/#add
ADD robot.py /robot/

CMD ["python", "robot/robot.py"]
