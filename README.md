# Scoring_API

* Implementation  the system of validating requests to the HTTP service API scoring.

To work with this service, install 2 packages pytest and redis
`pip install redis`
[redis](https://redis.io/)
`pip install pytest`
[pytest](https://docs.pytest.org/en/7.4.x/)

Run the program pass to the root of the program and run api.py
`python3 api.py`

to check the operability of the service in the terminal, type

```curl -X POST -H "Content-Type: application/json" -d '{
 "account": "horns&hoofs",
 "login": "h&f",
 "method": "online_score",
 "token": "55cc9ce545bcd144300fe9efc28e65d415b923ebb6be1e19d2750a2c03e80dd209a27954dca045e5bb12418e7d89b6d718a9e35af34e14e1d5bcd5a08f21fc95",
 "arguments": {
  "phone": "89998969999",
  "email": "volodya@mail.ru",
  "first_name": "Volodya",
  "last_name": "Gerochevich",
  "birthday": "01.02.2000",
  "gender": 1
 }
}' http://127.0.0.1:8080/method/```


if the service is working fine, the answer will be as follows
{"response": {"score": 5.0}, "code": 200}%
