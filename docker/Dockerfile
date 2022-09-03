FROM golang:1.19

# create a "place" in the docker image to store our code
WORKDIR /backend

# copy package management file first
COPY ./backend/go.mod ./
# COPY ../backend/go.sum ./

# download all depency packages
RUN go mod download

# copy source code
COPY ./backend/*.go ./

# build source code to executable file named backend-exec
RUN go build -o /backend-exec

CMD [ "/backend-exec" ]