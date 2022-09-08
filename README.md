afterlogic/docker-aurora-corporate-legacy
=========================================

Out-of-the-box [Afterlogic Aurora Corporate](https://afterlogic.com/aurora) image

Includes Apache, MySQL and PHP setup based on [fauria/docker-lamp package](https://github.com/fauria/docker-lamp). Contains improvements [offered for Aurora Files](https://github.com/extbe)

**NB:** This is a legacy edition of Docker image, Ubuntu and Apache are used, with MySQL in the image as well. The image will not be receiving updates as of September 2022. If you're looking for an up-to-date lightweight image, see [afterlogic/docker-aurora-corporate](https://hub.docker.com/repository/docker/afterlogic/docker-aurora-corporate) ([source on GitHub](https://github.com/afterlogic/docker-aurora-corporate))

Creating the image
------------------

	docker build -t afterlogic/docker-aurora-corporate-legacy .


Running docker image
--------------------

Start your image binding the external port 80:

	docker run -d -p 80:80 afterlogic/docker-aurora-corporate-legacy

and access the container via web browser at http://localhost/


Alternately, you can use any other port available, e.g. 800:

	docker run -d -p 800:80 afterlogic/docker-aurora-corporate-legacy

and access the installation at http://localhost:800/


Accessing admin interface
------------------------------

To configure Aurora Corporate installation, log into admin interface using main installation URL and `/adminpanel` path.

Default credentials are **superadmin** login and empty password.

Overriding configuration
------------------------------

To override Aurora Corporate configuration, put config files with overrides into `data/settings/` or 
`data/settings/modules/`. The file names must be the same as the ones you want to override.

Licensing Terms & Conditions
----------------------------

Content of this repository is available in terms of [AGPLv3 license](http://www.gnu.org/licenses/agpl-3.0.en.html) (see `LICENSE` file)
