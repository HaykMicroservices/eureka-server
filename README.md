# eureka-server

>With Eureka Server we don't take data from other microservice by url which set in our configs or in other fils. we take data from other services(micro) by they names
> we used to do it by ${address.service.url} it take value from config file (address.service.url=http://localhost:8082/api/address)
>
>but now we do it @FeignClient(value = "address-service",	path = "/api/address") instead @FeignClient(url="${address.service.url}", value="anyName")


![Screenshot from 2022-10-12 23-50-42](https://user-images.githubusercontent.com/115641332/195449835-bf3b40b7-3c40-48f5-b66a-0729252421ff.png)
