---
title: Basics
taxonomy:
    category:
        - docs
child_type: docs
---

### Chapter 1

# Basics

Discover the **basic** principles
<pre><code class="lang-csharp">
~~~scala
/**
    * Performance-oriented implementation using Java's StringBuilder with a precalculated initial size large enough
    * to avoid any additional allocations that can otherwise result from using append() during initialization.
    *
    * @return returns a command string ready to be sent to a terminal emulator program.
    */
def render: String = {
  // create a StringBuilder large enough to avoid reallocation from subsequent calls to append()
  val s = new StringBuilder(signature.length + (data.length * 4)).append(signature)
  val c = data.length - 1

  // loop thru the data parameters and append each one (plus a delimiter) to the buffer
  for (i ← 0 to c) {
    s append data(i)
    if (i < c) s append delimiter     // skip the final delimiter
  }
  s.append(terminator).toString
}~~~
</code></pre>