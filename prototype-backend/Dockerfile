FROM npm-base-image
RUN git clone https://github.com/LVM-IT/prototype-backend.git
RUN cd prototype-backend && npm install
CMD cd prototype-backend && npm run start
EXPOSE 8080