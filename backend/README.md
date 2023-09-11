# How to quickly build frontend over backend api without yaml only


## Use prism framework
```
https://meta.stoplight.io/docs/prism/674b27b261c3c-prism-overview
```

`prism mock -p 8080 openapi.yml`

# Use header Prefer: example or code 

```
curl http://localhost:8080/jobs
```

```
curl -H "Prefer: example=two-items" http://localhost:8080/users/1/job-applications 
```


```
curl -H "Prefer: example=two-items" http://localhost:8080/users/123/job-applications 
curl -H "Prefer: example=many" http://localhost:8080/users/1/job-applications 
```

Prefer code:

```
curl -H "Prefer: code=404" http://localhost:8080/users/1/job-applications 
```

`prism mock -p 8080 03.yml`
```
curl -H "Prefer: code=404" http://localhost:8080/foo 
```

# Use docker file
```
docker compose -f docker-compose.yaml up
```