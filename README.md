This repo contains a very simplified version to run a Collabora setup with Nextcloud. It is meant for local development and testing only.

It uses docker-compose to start a Nextcloud instance with the richdocuments app and a Collabora Online server.

## Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/juliusknorr/richdocuments-compose
   cd richdocuments-compose
   ```

2. Clone the richdocuments app and build it according to the development setup documentation https://github.com/nextcloud/richdocuments

3. Start the services using docker-compose:

   ```bash
   docker-compose up -d
   ```

4. Access Nextcloud at `http://localhost:8080` and log in with the credentials:
   - Username: `admin`
   - Password: `admin`

5. Enable the richdocuments app (user facing name is Nextcloud Office)
6. Configure the Collabora Online server in Nextcloud settings to point to `http://collabora:9980` (This is the the hostname used to access the Collabora container from within the Nextcloud container)
7. You should now be able to create and edit documents in Nextcloud using Collabora Online.
