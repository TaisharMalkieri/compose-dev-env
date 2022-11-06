FROM continuumio/miniconda3 as development
WORKDIR /code/dev
COPY . .

FROM build AS development
RUN apt-get update \
    && bash ./shell/utilities.sh
