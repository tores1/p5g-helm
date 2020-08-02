FROM node:14.5.0-alpine3.12

RUN apk update && apk add git && \
	git clone --branch v1.2.4 https://github.com/open5gs/open5gs.git && \
	rm -rf /open5gs/configs/* && \
	rm -rf /open5gs/debian/* && \
	rm -rf /open5gs/docker/* && \
	rm -rf /open5gs/docs/* && \
	rm -rf /open5gs/lib/* && \
	rm -rf /open5gs/misc/* && \
	rm -rf /open5gs/src/* && \
	rm -rf /open5gs/subprojects/* && \
	rm -rf /open5gs/tests/*

WORKDIR /open5gs/webui

RUN npm install && \
    npm run build

CMD npm run start

EXPOSE 3000
