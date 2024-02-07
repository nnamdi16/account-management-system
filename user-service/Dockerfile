#Vertex version
FROM vertx/vertx4

ENV VERTICLE_NAME com.nnamdi.user_service.MainVerticle
ENV VERTICLE_FILE target/user-service-1.0.0-SNAPSHOT.jar


# Set the location of the verticles
ENV VERTICLE_HOME /usr/verticles



EXPOSE 8082

# Copy your verticle to the container                   (2)
COPY $VERTICLE_FILE $VERTICLE_HOME/


# Launch the verticle
WORKDIR $VERTICLE_HOME
ENTRYPOINT ["sh", "-c"]
CMD ["exec vertx run $VERTICLE_NAME -cp $VERTICLE_HOME/*"]
