MPICXX = mpic++
SRC= $(wildcard *.cpp)
OBJ= $(SRC:.cpp=.o)
EXEC= main

%.o: %.cpp
	$(MPICXX) -o $@ -c $< 

main: $(OBJ) 
	$(MPICXX) -o $@ $^

run: main
	mpirun -np 4 ./main 4

clean:
	@rm -rf *.o

cleanall: clean
	@rm -rf $(EXEC)
