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
    https://raw.githubusercontent.com/littlecodersh/EasierLife/master/Plugins/Tuling/tuling.json \
    # Main script behind itchat robot
    # https://gist.github.com/littlecodersh/ec8ddab12364323c97d4e36459174f0d
    https://gist.githubusercontent.com/littlecodersh/ec8ddab12364323c97d4e36459174f0d/raw/73017604aef437970d5c441923cd6bc58e9b8f57/main.py

CMD ["python", "robot/main.py"]
