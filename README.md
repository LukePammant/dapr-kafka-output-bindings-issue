# dapr-kafka-output-bindings-issue

A simple project example to show the `ERRO[0007] error from c: no topics provided` error with output bindings. This project is based on the React started template generated using `dotnet new react`. 

You can see the issue by running the `dapr-run.bat` command. You can observe in the daprd window that it spams the error. Also you can see in the `dotnet run` window that `OPTIONS: /newUser - 200` is called even though the Kafka binding is a publisher and not a consumer. 

If the `app.UseSpa(*/...*/)` is commented out in the Startup.cs the daprd instance works fine.