FROM trch/erlang:25.0.4-alpine

ENV OTP_VERSION="25.0.3" \
    REBAR3_VERSION="3.18.0"

LABEL org.opencontainers.image.version=$OTP_VERSION

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=1001
ARG GRPNAME=vscodegrp

ENV DEBIAN_FRONTEND=noninteractive

RUN addgroup -g $USER_GID $GRPNAME \
    && adduser -u $USER_UID -g $GRPNAME -D $USERNAME
USER $USERNAME

CMD ["erl"]
