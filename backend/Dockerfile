# Bygger det med golang image
FROM golang:1.16-alpine 

# Laver og sætter workdir til /app fordi mod.go må ikke ligge på root
WORKDIR /app

# Kopier alt backend folderen ind i containers folder
COPY . .

# downloade requirements fra go mod filen
RUN go mod download

# Kører en go build for at bygge programmet (Det skal compile)
RUN go build

# Bruger Entrypoint i stedet for CMD fordi at ENtrypoint bliver ikke ændret
ENTRYPOINT ["go", "run", "backend"]

