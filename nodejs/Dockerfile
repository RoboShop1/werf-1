ARG BUILDER_IMAGE
FROM ${BUILDER_IMAGE} AS build


FROM alpine
WORKDIR /app
RUN apk update && apk add nodejs npm
COPY --from=build /app/server.js .
COPY --from=build /app/node_modules node_modules
CMD ["node","server.js"]




