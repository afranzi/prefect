---
sidebarDepth: 2
editLink: false
---
# Executors
---

## Functions
|top-level functions: &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|:----|
 | <div class='method-sig' id='prefect-utilities-executors-timeout-handler'><p class="prefect-class">prefect.utilities.executors.timeout_handler</p>(fn, *args, timeout=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/utilities/executors.py#L224">[source]</a></span></div>
<p class="methods">Helper function for implementing timeouts on function executions.<br><br>The exact implementation varies depending on whether this function is being run in the main thread or a non-daemonic subprocess.  If this is run from a daemonic subprocess or on Windows, the task is run in a `ThreadPoolExecutor` and only a soft timeout is enforced, meaning a `TimeoutError` is raised at the appropriate time but the task continues running in the background.<br><br>**Args**:     <ul class="args"><li class="args">`fn (callable)`: the function to execute     </li><li class="args">`*args (Any)`: arguments to pass to the function     </li><li class="args">`timeout (int)`: the length of time to allow for         execution before raising a `TimeoutError`, represented as an integer in seconds     </li><li class="args">`**kwargs (Any)`: keyword arguments to pass to the function</li></ul>**Returns**:     <ul class="args"><li class="args">the result of `f(*args, **kwargs)`</li></ul>**Raises**:     <ul class="args"><li class="args">`TimeoutError`: if function execution exceeds the allowed timeout</li></ul></p>|

<p class="auto-gen">This documentation was auto-generated from commit <a href='https://github.com/PrefectHQ/prefect/commit/n/a'>n/a</a> </br>on January 15, 2020 at 16:03 UTC</p>