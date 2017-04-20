# java-task-queue
A simple task queue system for Java. 
Don't be mad at me for this, it was done in ~10 minutes, but it seems to work pretty well. 
If you see anything that could be done better feel free to do pull requests. 

**Information**
Each queue will run one task at a time.  
The tasks with highest priority will of course be ran first. 

**Priority levels**
These are the defaults, but feel free to edit TaskPriority.java for your need.  
The priority is read in chronological order from TaskPriority, assuming the first is the highest and the last is the lowest. 
* LOWEST
* LOW
* MEDIUM
* HIGH
* HIGHEST

**A useless but somewhat clarifying example**
*The point is that you can extend or change the work() method of the task object, then you can run a custom task.*
```java

public static void main(String[] args) {

  //The queue will always wait for tasks in the background, so we might as well run it now. 
  Queue queue = new Queue();
  queue.run(); 
  
  // This will make the queue run a task. 
  Task task = new Task(TaskPriority.HIGHEST);
  queue.addTask(task);

}

```

