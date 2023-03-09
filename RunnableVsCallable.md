## Runnable Vs Callable

Both interfaces are designed to represent a task that can be run by multiple threads. 
We can run Runnable tasks using the Thread class or ExecutorService, 
whereas we can only run Callables using the latter. 


# Runnables

The Runnable interface is a functional interface and has a single run() method that doesn't accept any parameters or return any values.

This works for situations where we aren't looking for a result of the thread execution, such as incoming events logging:

public interface Runnable {
    public void run();
}

public class EventLoggingTask implements  Runnable{
    private Logger logger
      = LoggerFactory.getLogger(EventLoggingTask.class);

    @Override
    public void run() {
        logger.info("Message");
    }
}

public void executeTask() {
    executorService = Executors.newSingleThreadExecutor();
    Future future = executorService.submit(new EventLoggingTask());
    executorService.shutdown();
}

In this case, the Future object will not hold any value.

Since the method signature does not have the “throws” clause specified, we don't have a way to propagate further checked exceptions.


# Callables

The Callable interface is a generic interface containing a single call() method that returns a generic value V:

public interface Callable<V> {
    V call() throws Exception;
}

public class FactorialTask implements Callable<Integer> {
    int number;

    // standard constructors

    public Integer call() throws InvalidParamaterException {
        int fact = 1;
        // ...
        for(int count = number; count > 1; count--) {
            fact = fact * count;
        }

        return fact;
    }
}


@Test
public void whenTaskSubmitted_ThenFutureResultObtained(){
    FactorialTask task = new FactorialTask(5);
    Future<Integer> future = executorService.submit(task);
 
    assertEquals(120, future.get().intValue());
}


Callable‘s call() method contains the “throws Exception” clause, so we can easily propagate checked exceptions further: