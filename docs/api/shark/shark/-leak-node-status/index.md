[shark](../../index.md) / [shark](../index.md) / [LeakNodeStatus](./index.md)

# LeakNodeStatus

`enum class LeakNodeStatus`

### Enum Values

| Name | Summary |
|---|---|
| [NOT_LEAKING](-n-o-t_-l-e-a-k-i-n-g.md) | The instance was needed and therefore expected to be reachable. |
| [LEAKING](-l-e-a-k-i-n-g.md) | The instance was no longer needed and therefore expected to be unreachable. |
| [UNKNOWN](-u-n-k-n-o-w-n.md) | No decision can be made about the provided instance. |
