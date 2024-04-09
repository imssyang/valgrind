CFLAGS = -g -O0

%: %.c
	$(CC) -o $@ $^ $(CFLAGS)

run-%:
	valgrind --tool=memcheck --leak-check=yes --show-reachable=yes --num-callers=20 --track-fds=yes ./$*

.PHONY: clean
clean:
	rm -rf test
