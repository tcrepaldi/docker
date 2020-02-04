FROM openjdk:11 As build
WORKDIR build
COPY Main.java .
# Build Main.java
RUN javac Main.java

FROM openjdk:11-jre
# Copy resource from previous stage
COPY --from=build /build/Main.class .
# Run java code with the JRE
CMD ["java","Main"]