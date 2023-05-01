## Teoria
https://www.freertos.org/fr-content-src/uploads/2018/07/161204_Mastering_the_FreeRTOS_Real_Time_Kernel-A_Hands-On_Tutorial_Guide.pdf
### FreeRTOS Data Types
#### Ticks
- The tick count is used as a measure of time.
- Can be either an unsigned 16-bit type, or an unsigned 32-bit type
> Depending on the setting of configUSE_16_BIT_TICKS within FreeRTOSConfig.h
#### Function Names
- vTaskPrioritySet() returns a void and is defined within task.c.
- xQueueReceive() returns a variable of type BaseType_t and is defined within queue.c.
- pvTimerGetTimerID() returns a pointer to void and is defined within timers.c.
#### Creating Tasks
![[Pasted image 20230501003215.png]]
 - pvTaskCode
 > The pvTaskCode parameter is simply a pointer to the function that implements the task (in effect, just the name of the function).
 
 - pcName
>A descriptive name for the task. This is not used by FreeRTOS in any  way. It is included purely as a debugging aid. Identifying a task by a  human readable name is much simpler than attempting to identify it by its handle.
- usStackDepth
>Each task has its own unique stack that is allocated by the kernel to the  task when the task is created. The usStackDepth value tells the kernel how large to make the stack.
- pvParameters
>Task functions accept a parameter of type pointer to void ( void* ).
- uxPriority
> Defines the priority at which the task will execute. Priorities can be  assigned from 0, which is the lowest priority, to  (configMAX_PRIORITIES – 1), which is the highest priority.
- pxCreatedTask
>

- pdMS_TO_TICKS(int)
> nverts a time specified in milliseconds into a time specified in ticks. The resolution available depends on the defined tick frequency, and  pdMS_TO_TICKS() cannot be used if the tick frequency is above 1KHz

#### Sinchronization
FreeRTOS queues, binary semaphores, counting semaphores, mutexes,recursive mutexes, event groups and direct to task notifications can all be used to create synchronization events.



## Linux
https://github.com/vsserafim/twotasks-posix-gcc/blob/main/src/main.c
>Ejemplo compatible linux: https://www.youtube.com/watch?v=wZmXPj1YvBg




