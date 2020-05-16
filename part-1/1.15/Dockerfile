FROM node
WORKDIR /app
RUN npm install -g create-react-app
RUN npx create-react-app countryinfo
COPY countryinfo/src /app/countryinfo/src
COPY countryinfo/package* /app/countryinfo/
WORKDIR /app/countryinfo
RUN npm install
EXPOSE 3000

ENV REACT_APP_API_KEY=fc4c7ddce4ecf974fc4755ad1b208dff
CMD npm start