# in short #
![https://corkami.googlecode.com/svn/wiki/pics/seh_flowchart.png](https://corkami.googlecode.com/svn/wiki/pics/seh_flowchart.png)
  1. an exception handler is set up (there's always a default one by the OS)
  1. an exception happens
  1. control is tranferred to the handler
    1. the handler can read and write the context (ie, all the registers) of the code when the exception was triggered
  1. the handler returns, telling the OS whether it handled it or not.
  1. if the exception is considered handled, the thread resume according to the (updated) context

## triggers ##
  * exceptions are triggered when something 'wrong' happens during code execution.
> > ![https://corkami.googlecode.com/svn/wiki/pics/seh_divzero.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_divzero.gif) ![https://corkami.googlecode.com/svn/wiki/pics/seh_intof1.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_intof1.gif)
> > ![https://corkami.googlecode.com/svn/wiki/pics/seh_invmem.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_invmem.gif) ![https://corkami.googlecode.com/svn/wiki/pics/seh_privins.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_privins.gif)
> > ![https://corkami.googlecode.com/svn/wiki/pics/seh_trig_inv.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_trig_inv.gif)
    * or some specific triggers are called
> > ![https://corkami.googlecode.com/svn/wiki/pics/seh_bpint_3.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_bpint_3.gif) ![https://corkami.googlecode.com/svn/wiki/pics/seh_bpint3.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_bpint3.gif)
> > ![https://corkami.googlecode.com/svn/wiki/pics/seh_ssicebp.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_ssicebp.gif)

  * the exception might happen:
    * before the current operation is executed (i.e. it's **NOT** executed, most likely because it can't)
    * after it's executed (like, an information signal)
    * or after the next instruction is executed (stepping exception)

  * the exceptions might be different depending on the OS or the configuration
    * ![https://corkami.googlecode.com/svn/wiki/pics/seh_privinsvmw.gif](https://corkami.googlecode.com/svn/wiki/pics/seh_privinsvmw.gif)
## handlers ##
  1. the system will handle it if no other code handled it before (it's a chain of handlers) - and typically just terminates the program.

  1. the handler is running on the same thread, but can read the context (values of all registers, including debug registers) of the thread when it happened, then modify this context, which will be taken into account when the handler finished its job.
# in details #
## set up ##
you can set a Vectored Exception Handler (one per thread) or a Structured Exception Handler (typically, per function).

VEH are set via APIs, but SEH are set directly via a few instructions.

FS is an obvious reference, but can be hidden...
  * via `fs:[0]`
  * via `fs:[18h]`
  * hardcoded value
    * read it via GetThreadSelectorEntry
  * pass to gs, ds...

Handlers get access to the context => easy and powerful way to modify your own thread without any API call
  * read/set registers values
  * read/set hardware breakpoint
    * detect debuggers
    * set them manually to reuse (ensure they're not used by a debugger)
  * read/set flag
    * read flags to 'emulate' conditional jump behavior (exception-controlled flow)
    * set trap flag manually to trigger an instruction after the next one is emulated

## tricks ##
  * skip ntdll
    * overwrite return address in stack, to return directly to expected URL
  * overwrite handler address in stack, trigger another exception


---

# acknowledgements #
  * Peter Ferrie

# Other resources #