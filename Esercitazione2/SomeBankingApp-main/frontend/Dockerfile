FROM node:20.19-alpine AS build
RUN apk add --no-cache git
WORKDIR /app
RUN git clone https://github.com/chaymahamidi/sss2026.git .
WORKDIR /app/Esercitazione2/SomeBankingApp-main/frontend
RUN npm install
RUN npm run build -- --configuration production
RUN find /app/Esercitazione2/SomeBankingApp-main/frontend/dist -maxdepth 4 -print && ls -la /app/Esercitazione2/SomeBankingApp-main/frontend/dist

FROM nginx:alpine
COPY --from=build /app/Esercitazione2/SomeBankingApp-main/frontend/dist/SomeBankingFrontend/browser /usr/share/nginx/html
EXPOSE 4200