# java-task-queue
A simple task queue system for Java. 
Don't be mad at me for this, it was done in ~10 minutes, but it seems to work pretty well. 
If you see anything that could be done better feel free to do pull requests. 

**Example usage**
```java

public static void main(String[] args) {
  Queue queue = new Queue();
  queue.run(); //The queue will always wait for tasks in the background, so we might as well run it now. 
  
  // This will make the queue run a task. 
  Task task = new Task(TaskPriority.HIGHEST);
  queue.addTask(task);
  
  // The point is that you can extend or change the work() method of the task object, then you can run a custom task. 
  
}

```

