# learn-pinia-setup

**Technologies:** VUEJS 3

## Initial Local Setup (Ubuntu)

### 1. Clone the Project

Clone this repository:

```
git clone <repo-url>
```

### 2. Start Containers

Navigate to the `docker-compose-vue` folder and start the containers in the background:

```
docker compose up -d
```

### 3. Access the Web Container

Launch Bash in the `vue` container:

```
docker compose exec vue bash
```

### 4. Install Dependencies and Run Project

Inside the vue container, install project dependencies:

```
npm install
```

Then, start the development server:

```
npm run dev
```

### 5. Configure Hosts File on Host Machine

Open `/etc/hosts`:

```
sudo nano /etc/hosts
```

Add the following line:
```
127.0.0.1   learn-pinia-setup.local
```

### 6. Visit the Vue.js application at `http://learn-pinia-setup.local:5173`

### 7. Change HTTP Port if Needed

If port 5173 is already in use (e.g., by an another application), you can change the HTTP port
HOST_MACHINE_UNSECURE_HOST_PORT in the .env file in the docker-compose-vue folder

#### Other commands
```
docker compose stop
docker compose start
docker compose down
docker compose up -d
docker compose exec vue bash
docker compose build --no-cache
```
