CC = mpicc
CFLAGS = -Wall -O2

PROGRAMS = sum_bcast sum_scatter sum_gather sum_reduce sum_allreduce sum_scan

all: $(PROGRAMS)

sum_bcast: ../Exercise01/sum_bcast.c
	$(CC) $(CFLAGS) -o sum_bcast ../Exercise01/sum_bcast.c

sum_scatter: ../Exercise02/sum_scatter.c
	$(CC) $(CFLAGS) -o sum_scatter ../Exercise02/sum_scatter.c

sum_gather: ../Exercise03/sum_gather.c
	$(CC) $(CFLAGS) -o sum_gather ../Exercise03/sum_gather.c

sum_reduce: ../Exercise04/sum_reduce.c
	$(CC) $(CFLAGS) -o sum_reduce ../Exercise04/sum_reduce.c

sum_allreduce: ../Exercise05/sum_allreduce.c
	$(CC) $(CFLAGS) -o sum_allreduce ../Exercise05/sum_allreduce.c

sum_scan: ../Exercise06/sum_scan.c
	$(CC) $(CFLAGS) -o sum_scan ../Exercise06/sum_scan.c

clean:
	rm -f $(PROGRAMS)

run:
	@echo "Running MPI programs with 4 processes..."
	mpirun -np 4 ./sum_bcast
	mpirun -np 4 ./sum_scatter
	mpirun -np 4 ./sum_gather
	mpirun -np 4 ./sum_reduce
	mpirun -np 4 ./sum_allreduce
	mpirun -np 4 ./sum_scan
