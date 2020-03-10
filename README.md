TL/DR: Keybindings for popular editors so you can quickly enjoy Arrow Key Debugging.

Update: Now live on [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=gilescope.arrowdebugging)!

# Arrow Debugging Manifesto

For too long now have our fingers suffered the indignity of being banished to the furthest outer reaches of the keyboard. Since eternity debugging has been regarded as a second class citizen, looked down upon by those who prefer to run the code by the power of thought alone. 

Fear not comrades, for the time has come to recapture the center ground of the keyboard (for Vi fans anyway) and improve our debugging ergonomics. Stop the contortion of limbs and rebind your keys to freedom. Contortions are replaced by a feeling of 'flow', - you don't even think about moving through the code. Mind and instruction pointer are one. Step In, Step Out, Step In, Step Out. Mr Miyagi would be proud.

Everyone has a keyboard, so _everyone_ can upgrade their debugging experience.

Rise up and surf the debugger!

## What is it?

Having discovered it worked so well and blogged about it last year ( http://gilescope.ninja/rust/2018/04/25/ArrowDebugging.html ), the next logical step is to make it easy for you too to experience the joy of ArrowDebugging.

Arrow Key Debugging is just what it says on the tin, but the state of being that it promotes is one that must be experienced for oneself. This mechanism of driving a debugger is far more ergonomic than using function keys.

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

## Time traveling

If you have the ability to time travel, hold down Ctrl as well as Alt when going Up or Down to move forwards and backwards through time.

## Paste

As a bonus, pasting (Alt-V) the current instruction pointer seems to also work pretty well.
(VSCode doesn't yet support setting the next statement, but recent pycharm relases can)

## VSCode

Currently it doesn't seem possible to undo keybindings in an extension, so you will have to paste these into your
keybindings.json manually for now:

```
{
    "key": "alt+right",
	"command": "-workbench.action.nextEditor"
},
{
	"key": "alt+left",
    "command": "-workbench.action.previousEditor"
}
```

## ViM Mode

Obviously life wouldn't be worth living if we didn't have Vi keybindings also. If you're stepping through a debugger in Vi (anything's possible in Vi) or if your in Vi mode for your favorite editor then you too can have arrow key debugging:

 ```
               Play on / Continue
                     Alt+K
                       ^
                       |
Step Out  Alt+H <--  --> Alt+L  Step In
                       |
                       V
                    Alt+J
                    Step Over
```

(Maybe we should have a vi branch to store these?)

## Apologies

Apologies to all the debugger implementers out there. Once someone is in the state of flow with the debugger, expectations of debugging speeds increase. We need faster debuggers! (Lldb's a great example of a fast debugger where stepping is quick - we're after the low hundreds of milliseconds ideally - you don't want to break the flow with a second pause.).

## Credit

Kudos to Ivan Moor and Kent Beck for getting people to focus on fixing the little things.

And prior art: kudos to anyone else who's undoubtably been doing this for years - I haven't found any prior art, though undoubtedly someone in the 70s will have beaten me to it... (Bet it was Dijkstra, he's always been quick off the mark!)

## PRs

Pull Requests welcome! Especially keen for designs of other types of debugging controllers:

   * Virtual Reality - Few have debugged in VR yet, what would the perfect debugging device look like? Personally I think a small lovable puppy that you hold in one hand and stroke with the other to step next could work...but am open to ideas!
   * Once the above PR lands, let's make one in real life. There should be dedicated hardware debugger controllers whether we repurpose console controllers, fancy mice or custom keyboards, let us make debugging a first class citizen.

![](https://www.maxpixel.net/static/photo/2x/Portrait-Dog-Animal-Stroke-Fur-Pet-Cute-3026154.jpg)

## Disclaimer

No parrots virtually alive or dead were harmed in the making of these keybindings.
