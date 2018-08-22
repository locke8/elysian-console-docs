---
title: '2.1 Get the Console'
taxonomy:
    category: docs
child_type: docs
visible: true
---

import econsole._

val con = econsole.get()

con << "Some black text on a white background".black.on.white + nl
