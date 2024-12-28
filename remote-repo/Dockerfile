ARG BUILDER_IMAGE
FROM ${BUILDER_IMAGE} AS builder

FROM docker.io/node:20-slim
COPY --from=builder /app/  /app1/
CMD ["node","/app/server.js"]