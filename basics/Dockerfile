FROM node:4.6 as build
WORKDIR /app
ADD . /app

FROM build as ut
RUN echo "unit test"

FROM build as static
RUN echo "coverage and static analysis"

FROM build as ui
RUN echo "UI tests"

FROM build as final
RUN echo "final artifact"

from node:4.6
RUN npm install
EXPOSE 3000
CMD npm start
