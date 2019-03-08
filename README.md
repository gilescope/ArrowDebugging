# ArrowDebugging
Keybindings for popular editors so you can quickly try out Arrow Debugging

## What is it?

Having discovered it worked so well and blogged about it (
http://gilescope.ninja/rust/2018/04/25/ArrowDebugging.html ), the next logical step is to make it easy for you to experience the joy of ArrowDebugging.

Arrow Key Debugging is just that. Kent Beck said once "focus on the small stuff". I think this mechanism of driving a debugger is more ergonomic than anything else I've seen out there.
 
 ```
               Play on / Continue
                     Alt+Up
                       ^
                       |
Step Out  Alt+Left <--  --> Alt+Right  Step In
                       |
                       V
                    Alt+Down
                    Step Over
```

## Paste

As a bonus, pasting (Alt-V) the current instruction pointer seems to also work pretty well.
