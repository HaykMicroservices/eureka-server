# eureka-server



>With Eureka Server we don't take data from other microservice by url which set in our configs or in other fils. we take data from other services(micro) by they names
> we used to do it by ${address.service.url} it take value from config file (address.service.url=http://localhost:8082/api/address)
>
>but now we do it @FeignClient(value = "address-service",	path = "/api/address") instead @FeignClient(url="${address.service.url}", value="anyName")


![Screenshot from 2022-10-12 23-50-42](https://user-images.githubusercontent.com/115641332/195449835-bf3b40b7-3c40-48f5-b66a-0729252421ff.png)

for run our microservice project without api gatway we have to run eureka-server, adress-service, student-service(without api gatway branch)

we have to request to student-service like this link http://localhost:8080/api/student/getById/2

we have to request to adress-service like this link http://localhost:8082/api/address/getById/1

## With api-gatway

>for run our microservice project with api gatway we have to run api-gatway, eureka-server, adress-service, student-service(with api gatway branch)

we have to request to student-service like this link http://localhost:9090/student-service/api/student/getById/1

we have to request to adress-service like this link http://localhost:9090/adress-service/api/adress/getById/1
