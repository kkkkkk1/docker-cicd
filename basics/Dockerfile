FROM node:4.6 as unit
WORKDIR /app
ADD . /app
RUN echo "unit test"

FROM node:4.6 as static
RUN echo "coverage and static analysis"

FROM node:4.6 as ui
RUN echo "UI tests"

FROM node:4.6 as final
RUN echo "final artifact"

from node:4.6
RUN npm install
EXPOSE 3000
CMD npm start
