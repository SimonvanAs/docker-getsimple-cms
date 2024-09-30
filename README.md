# docker-getsimple-cms

Docker image for GetSimple CMS, an XML based, stand-alone, fully independent and lite Content Management System (<http://get-simple.info/>).

This image sets up a development environment and relies on Debian Linux, Apache 2 and PHP8. Fork from mablanco

## How to use this image

This will start a GetSimple CMS instance listening on port 80:

    $ docker run -d -p 80:80 --name getsimple mablanco/getsimple-cms

If you'd like persistance, you can create a volume for that purpose:

    $ docker volume create getsimple_web
    $ docker run -d -p 80:80 --name getsimple -v getsimple_web:/var/www/html mablanco/getsimple-cms

Once the container is running for the first time, navigate to `/admin` to be redirected to the upgrade and install scripts.

### Docker-compose

September 30th, Will be added in a couple of days