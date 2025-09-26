a.out: client.cpp client.h ../common/CommandHandler.cpp ../common/CommandHandler.h
	g++ client.cpp ../common/CommandHandler.cpp -o a.out

debug: client.cpp client.h ../common/CommandHandler.cpp ../common/CommandHandler.h
	g++ -g -DDEBUG client.cpp ../common/CommandHandler.cpp -o a.out

run: a.out
	./a.out 127.0.0.1:5555 --dest-host 127.0.0.1 --dest-port 5432

run-debug: debug
	./a.out 127.0.0.1:5555 --dest-host 127.0.0.1 --dest-port 5432

clean: 
	rm a.out
	rm client_storage/server.txt

# exClient: exClient.cpp
# 	g++ exClient.cpp -o exClient
# exServer: exServer.cpp
# 	g++ exServer.cpp -o exServer
# run: exClient exServer
# 	./exClient localhost
# clean:
# 	rm exClient
# 	rm exServer
# 	rm *.o
