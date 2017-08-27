# threadpool_lib
Threadpool Library w/ Simple Test
Co-created with [Salim Salaues](https://github.com/ssalaues)

We were assigned a task over the weekend to create a basic multi-threaded library in C with a few basic functions. Our functions include:
- Create Thread
- Add Task

As we explored the concept of multi-threading we realized we would need a highly specialized *.h* file. This file would have to include a few very specific structs that wold allow us to manipulate the tasks correctly.
![alt text](https://github.com/jeftekhari/threadpool_lib/blob/master/pics/header.png "header")

Above you'll see that we have 3 structs. `job`, `job_type`, and `tp_thread`. We also use the `pthread.h` library which comes with it's own `pthread_t` data type.

![alt text](https://github.com/jeftekhari/threadpool_lib/blob/master/pics/driver.png "driver")

At the start of our driver, we initialize 8 threads by using the `ft_tp_create` function. We then give some text to each job type.

![alt text](https://github.com/jeftekhari/threadpool_lib/blob/master/pics/create.png "thread pool create")

Then comes the add task function!

![alt text](https://github.com/jeftekhari/threadpool_lib/blob/master/pics/addTask.png "add task")

Finally, after we've allocated all the memory we'll need to use our threads, we need to set up the queue. The queue is important for a couple reasons. The purpose of multithreading is to able to do multiple calculations at the same time. Normally, in C, the code runs synchronously. This means that your program will run in the exact order that you define, unless you specifically tell it not to.

Our queue allows calculations to run independent of each other. If we run three threads and the third thread finishes first, it will wait for the other two threads to finish before it finishes. This allows us to maximize our computing power, while still maintaining order.

![alt text](https://github.com/jeftekhari/threadpool_lib/blob/master/pics/Queue.png "queue")

And thats it! Thanks for reading.

## Challenges / Learning Opportunities
- Understanding Multithreading and Processing Power
- Complex header and structs
- Group Work and Deadlines
