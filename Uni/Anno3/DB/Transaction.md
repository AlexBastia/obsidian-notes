> Set of non-detachable (atomic) operations that are correct even on a concurrent system, with final effects.

A single transaction is made of many related operations that are either performed as a whole or not at all. They must also be coherent when concurrent.

A transaction is *committed* only when the final result is logged and tracked, even when failures occur.