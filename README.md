# NugMacro-Keypad
 This is my first (working)attempt at designing/assembling a keyboard from scratch.
 I'll try to include some issues I had, and how I resolved them for others to look at when troubleshooting their own designs, and for myself.
 
### Before We Get Into Issues/Disclaimer
 For anyone reading this trying to troubleshoot their own project. If you have not realized this yet, especially if this is your first attemp at something like this, realize  that troubleshooting will be the most time consuming part of this. After all, it's always a learning experince, and thats just the nature of it.
- **Disclaimer** to anyone reading this. My understanding is that this project uses a bit of outdated components with the mcu, power connector, and daughterboard as theres definetely better MCU options and now better daughterboard options. I originally began this in 2020, so please don't use my schematic or parts list as a bible for building your own.

### Learning How To Use KiCAD
- The popular EDA of choice is [KiCAD](https://www.kicad.org/). It's free and not incredibly hard to learn. 
- YouTube videos worked best for me to get started.
- Going through KiCAD's doc page is incredibly helpful for any issues videos can't help you solve.
- Like with any new software, it's going to take a lot of time to really understand it, but try not to get discouraged.
 
### Schematic Issues
- Try to keep everything organized for yours, and others sake.
- Flags are your friend for organization.
- Try to look at it from the perspective of someone else every now and then. Noone wants to try to understand a shitty schematic, and if you take a long break from working on it, it's a pain in the ass to know what you were doing (Learned this the hard way).
- For footprints and symbols, there are some great libraries from people like [Ai03](https://github.com/ai03-2725) and [EBastler](https://github.com/ebastler). You can learn to make your own, but for your first attempt theres not a whole lot of reason to do that to yourself.
- When actually choosing your components, look at the datasheet for your chosen MCU. It's got everything you need to know for the basic requirements.

### PCB Issues
- If you already know how you want the outline of your PCB to look like, make sure your components will fit into this well to make it easy to route later.
- For USB connections, route your data lines in a close to equal length, with no other traces under or over them.
- Make your traces and layout look good. Your spending a lot of time to create this, and when you finally see the physical result, you want it to look intentional and thoughtful.
- Try to keep your crystal close to your MCU, and keep other traces away from it if they don't need to be there. A ground fill around it is also good for reducing possible interference.
- This took me longer to realize than it should have, but don't try to connect the ground net through a messy spiderweb of traces. Use a ground fill.
- Orient your MCU in whatever way makes it easist, and  prettiest, to route.

### Adding Artwork
- If you want, you can add drawings or other symbols/lettering to your silkscreen using something like [SVG to Shenzen](https://github.com/badgeek/svg2shenzhen).

### Manufacturing
- I ordered my boards from [JLCPCB](https://jlcpcb.com/).
- When making the production files, there are plugins for KiCAD that can make this easier, but just make sure you verify it looks correct.
- When selecting components for assmebly, make sure they are all correct. I had an issue from choosing a crystal at the correct speed, but wrong load.
- I used this formula **_(CL = (C1 * C2) / (C1 + C2) + Cstray)_** for finding what load rating I needed for my crystal. C1 and C2 are the caps for your crystal and I used **5pF** for my stray approximation.
- **For the love of god** do not try to assemble the entire board yourself thinking it wont be that hard.
- After you buy all the parts, ship everything, and assemble it. The time and money spent is not worth getting at least the majority of the board assembled form JLC.
- Especially if you try to do this all with a soldering iron, it can definetly be done, but there is a *__Lot__* of room for mistakes
- I did it thinking it would be good experince, and thinking it would be cool to do it all myself. It wasn't, mistakes are expensive, a lot can and did go wrong for me, and soldering experince will in no way make you immune to these mistakes.
- Given all of that, it is kinda fun doing it all yourself.
- And for components, I just uploaded my BOM to [DigiKey](https://www.digikey.com/) and ordered from them.
### Writing The Code
- I'll add info on this later, sorry.




### Case and Plate
- If you 3D print this yourself, make sure you have a well calibrated printer.
- I opted to use a piece of FR4 that I then lasercut to size.
- You can use a plate generator like this one from [swillkb](http://builder.swillkb.com/) to make it easier.
- I am currently working on a walnut case for my board, but when designing your case. Make sure you account for your desired mounting style, and daughterboard or any additional components you may have.

 ### Notes
 - I'll add some helpful links later.
 - I'll get these files organized a bit better/remove a good bit of junk soon.
 - Prob need to condense/organize this better.
 - If anyone has any questions about your own project or mine. Shoot me an email (Logan@Scootah.dev) and I'll do my best to give you a good answer.
