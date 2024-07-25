# Pipeline architecture

Comprises of filter and pipes (Unix shell).

## Filters (command)

- One and only one task
- Self-contained
- Stateless

### Examples

- **Producer** - Start of the workflow. Also called *source*.
- **Transformer** - Accespts data input, transorms the data, pass the transformed data to the next filter.
- **Consumer** - The last stage of the workflow. Also called *termination point*.

##  Pipes (|)

- Communication channel between the two filters.
- Uni-directional.

## Variations

- **One-to-many**
  A filter sends the *same* data to multiple filters downstream. Think of `tee` command.
- **Many-to-one**
  Multiple filters send data (possibly *different*) to one filter downstream. Think of it as an aggregator.

## Good 
- Simple
- Well understood
- Low cost
- Modular