FROM continuumio/miniconda3 AS build
WORKDIR /anaconda/src/
COPY . .

FROM build AS development
RUN bash ./shell/utilities.sh

FROM alpine:3.12
EXPOSE 8000
COPY --from=build / /server
CMD ["/server"]
