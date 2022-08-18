# Bygger det med golang image
FROM golang 

# Laver og sætter workdir til /app fordi mod.go må ikke ligge på root
WORKDIR /app

# Kopier alt backend folderen ind i containers folder
COPY . .

# Kører en go build for at bygge programmet (Det skal compile)
RUN go build

# Bruger Entrypoint i stedet for CMD fordi at ENtrypoint bliver ikke ændret
#hihi
ENTRYPOINT ["go", "run", "backend"]

