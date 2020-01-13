## The Game Development Process
Obviously, the process of developing a game is exceedingly long & intricate. However, this section aims to capture the essentials that form this process.

1. Pre-production. At this point, no code is being written. The team brainstorms for ideas, toys around with varying concepts, possibly comes up with some intial designs, & a production plan is at least created.
2. Production. This stage forms the large majority of the Game Development Process. It is during this stage that all the design details related to the game are fleshed out, the actual logic is implemented, etc. The end of this stage is typically testing of the game.
3. Post-production. This stage includes the required steps to take the game live. It includes actually shipping the game, as well as the long-term maintenance work that will be required by the game.

## Windows Programming
In this module, we will be building games for the Windows operating system. Hence, we can expect to work not rarely with the Windows SDK. This section includes notes for the Windows SDK.

### Data types
The Windows SDK is chock-filled with all kinds of data types. Find an exhaustive guide [here](https://docs.microsoft.com/en-us/windows/desktop/winprog/windows-data-types).

Note that the Windows SDK provides a typedef, `BOOL`, that holds 2 possible integers. `TRUE` represents the integer value 1 & `FALSE` represents the integer value 0. 2 things to take note of here - (a) that this `BOOL` type isn't interchangeable with the `bool` type in cpp & (b) that most integer-functions use any non-zero value to indicate success. Therefore, avoid using `if (result == TRUE)` to check for the success of a function's invokation. Rather, `if (result)` is preferable.

#### Windows
Your Windows application will, most likely, be made of Windows. Within your application code, each of these Windows are accessed by a **handle**. Any operation to be performed on a Window will be operating on a Window's handle. Do note that handles **aren't** pointers. 

## Random notes
- In C++, NULL is equal to the integral value of 0.
The `main` function that we are used to making use of in cpp applications is replaced by `WinMain` in Windows Programming. The `WinMain` function contains a message loop that iterates continuously, ready to receive & process messages, until it receives a `WM_QUIT` message.
