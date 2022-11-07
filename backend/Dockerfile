FROM build AS development
ENV RUNNING_IN_DOCKER=true

RUN bash ./shell/utilities.sh
COPY .config/zsh/.zshenv .
RUN bash ./shell/shell.sh


FROM continuumio/miniconda3 AS build
COPY . .

FROM alpine
EXPOSE 8000
COPY --from=build /opt/conda /opt/conda
ENTRYPOINT [""]