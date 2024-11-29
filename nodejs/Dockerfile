ARG BUILDER_IMAGE
FROM ${BUILDER_IMAGE} AS build


FROM alpine
WORKDIR /app
COPY --from=build /app/server.js .
COPY --from=build /app/node_modules node_modules
CMD ["node","server.js"]