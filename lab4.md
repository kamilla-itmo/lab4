## Отчет
1. Создала dockerfile
2. Построила образ : sudo docker build . -t aafire
3. Создала 2 контейнера : sudo docker run -t --name aafire1 aafire ; sudo docker run -t --name aafire2

   ![скриншот](https://github.com/kamilla-itmo/lab4/blob/main/fire.png)

4.Повторно запустила эти контейнеры : sudo docker exec aafire1 aafire2

5.Создала сеть между контейнерами : sudo docker network create myNetwork

6. Подключила оба контейнера к созданной сети :

                                                docker network connect myNetwork aafire1
                                                docker network connect myNetwork aafire2
   
7. Проверила соединение между контейнерами при помощи утилиты ping , но произошла ошибка. 
