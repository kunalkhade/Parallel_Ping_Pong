# Parallel_Ping_Pong

Design two different processes A and B which are running independently on
different computers. First process A will send message to process B and then
B will message back to A. Depending on the timing, communication cost will
estimate. Assume, time needed to send an n-byte message is λ + η/β
where, λ = Latency, β = Bandwidth, η = Byte Message

Write distributed memory program and determine latency and bandwidth.
Process A will record time and then send a message to process B. after process
B will send it back to process A. Process 0 receives message and record the
time. The elapse time divided by 2 is the average message passing time. Send
message multiple time and experiment with message of different lengths, to
generate enough data points and estimate latency and bandwidth using linear
regression
Use blocking, non-blocking send and receive, as well as the MPI SENDRECV()
function.

# Algorithm and libraries
MPI Send has four modes of communication: Standard, Buffered, Synchronous,
and Ready and each of these can be blocking and non-blocking. Receive has
only one mode and can be blocking or non-blocking.
After initializing all parameters of MPI i allocated different memory size for the
variable in for loop. It is an iterative loop of 28 count which help to allocate
different memory size using malloc function. Process A send data in the memory
and Process B will receive it. Time period calculated using the MPI Wtime
function. Same operation perform 10 times and at the end time value divide by
10*2. After further computation we get other parameters bandwidth, latency
etc.
# Program is design as follows :
1) Initialize all MPI parameters.
2) Add boundary condition which will scan the input processes and confirm
that it has to be 2.
3) Opening FOR loop with count of 0-27. It allocate memory and in every
iterative loop it increases size of memory allocation.
4) Initialize loop counter(10) and Start with MPI clock to measure the
execution time and check time difference between message passing between
two processes.
5) Calculate Bandwidth and Latency of parallel loop.
6) Display using Printf and terminate MPI process using MPI Finalize
function.

