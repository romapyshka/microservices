git clone --recurse-submodules https://github.com/romapyshka/microservices.git

docker compose up 

After this you can send POST request to:
'localhost:3000/user'

Body:
    {
        username: "Roman"
}

You should receive this answer:
[{
    message: Notification was send to Roman!
    user: {
        id: 1
        username: Roman
}
}]

In this web-site you can see notification that will be sent to user after 24 hours

https://webhook.site/#!/view/f6e50b78-c54d-4409-a910-13dca6241000/189770e8-06ae-4666-8b4c-2f61bb4a96e0/1

For schedule notification I used two methods: SetTimeout and library Bull.js that works with Redis and can make queue

For more details visit web-site of documentation: https://github.com/OptimalBits/bull



