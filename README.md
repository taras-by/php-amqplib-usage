# php-amqplib usage
https://github.com/php-amqplib/php-amqplib

Install:

    $ docker-compose build
    $ docker-compose up -d
    $ ./docker/app composer install
    
Commands:
    
    $ ./docker/start
    $ ./docker/stop

## Code

[Tutorial one: "Hello World!"](https://www.rabbitmq.com/tutorials/tutorial-one-php.html):

    ./docker/app php send.php
    ./docker/app php receive.php


[Tutorial two: Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-php.html):

    ./docker/app php new_task.php "A very hard task which takes two seconds.."
    ./docker/app php worker.php


[Tutorial three: Publish/Subscribe](https://www.rabbitmq.com/tutorials/tutorial-three-php.html)

    ./docker/app php receive_logs.php
    ./docker/app php emit_log.php "info: This is the log message"

[Tutorial four: Routing](https://www.rabbitmq.com/tutorials/tutorial-four-php.html):

    ./docker/app php receive_logs_direct.php info
    ./docker/app php emit_log_direct.php info "The message"


[Tutorial five: Topics](https://www.rabbitmq.com/tutorials/tutorial-five-php.html):

    ./docker/app php receive_logs_topic.php "*.rabbit"
    ./docker/app php emit_log_topic.php red.rabbit Hello

[Tutorial six: RPC](https://www.rabbitmq.com/tutorials/tutorial-six-php.html):

    ./docker/app php rpc_server.php
    ./docker/app php rpc_client.php
    