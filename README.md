# spring-gumball CI/CD Lab Notes

## Part 1: CI
First, I cloned over the repo and set up the CI action on Github. 

I had to update the file as my Github account hasn't updated master to main yet

![yml file updatefd](screenshots/gradle-yml.png) 

![CI](screenshots/ci.png)

## Part 2: CD

Then, I moved over and set up the service account on GKE with the key

![service account keys](screenshots/service-acc-keys.png)

I set up a cluster and updated my yaml file

![yaml file updated](screenshots/GKE-yaml.png)

And migrated that over to my github. I forgot to base64 encode the key and for some reason the github action didn't put the yml file in the right location at first, so it took a couple tries to get that up

![cd](screenshots/cd.png)

![secrets in github](screenshots/github-secrets.png)

![github actions](screenshots/actions.png)

From there, I checked on GKE to confirm it worked, which it did.

![cluster](screenshots/cluster.png)

![service](screenshots/service.png)

![deployment](screenshots/deployment.png)

So I created a load balancer...

![setup load balancer](screenshots/create-lb.png)

![ingress](screenshots/ingress.png)

And hit the endpoint successfully!

![homepage up and running](screenshots/homepage.png)

Lab complete!
