# Bygger det med golang image
FROM golang 

# Laver og sætter workdir til /app fordi mod.go må ikke ligge på root
WORKDIR /app

# Kopier alt backend folderen ind i containers folder
COPY . .

# Kører en go build for at bygge programmet (Det skal compile)
RUN go build

# Expose er bare noget der fortæller hvilen port man skal kigge efterq
EXPOSE 8080

# Bruger Entrypoint i stedet for CMD fordi at ENtrypoint bliver ikke ændret
ENTRYPOINT ["go", "run", "frontend"]
