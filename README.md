# JEB Incubator Platform

## Production deployment guidelines

Fill in the necessary information in the `.env`  
You can find a template in `.env.template`

To start the full product:
```bash
docker compose --profile backend --profile frontend up
```

## Development environment guidelines

You can start only specific part of the platform stack using the profile feature of the provided `docker-compose.yml`
For example to work on the backend you can start only the frontend and the db with the following command.
```bash
docker compose --profile db --profile frontend up
```
> Don't forget to fill the development .env file used by the backend that can be found at `backend/.env.template`

The same thing applies if you want to work in real-time on the frontend, you can start only the backend
```bash
docker compose --profile backend up
```

## URL(s)

`<root>` Main platform access  
`<root>:8080` Proxy dashboard  
`<root>/api` Backend API  
`<root>/api/docs` Swagger UI with the backend OpenAPI v3  
`<root>/api/dashboard` Grafana dashboard to show metrics about the backend  
