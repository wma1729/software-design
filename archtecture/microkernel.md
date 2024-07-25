# Microkernel (plug-in) architecture

## Main components

### Core system
The core system provides the minimal functionality.

### One or more plug-ins
The extensibility, adaptability and isolation is provided by the plug-ins. For example, reading from files, database, and sockets via 3 different plug-ins.

### Registry
The means by which the core system discovers what plug-ins are available.

### Contract
The contract between the core system and the plug-in components. The **control** contract is usually provided by interfaces that are implemented by the plug-ins. The **data** contract is provided by some sort of data schema like json schema, etc.

## Good
- Simple
- Well understood
- Low cost
- Modularity