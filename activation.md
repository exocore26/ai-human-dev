
### Activation — From Intent to Genesis

Activation is a lightweight assignment engine that turns an intention into a structured, traceable starting point for work.

An assignment can be created for any of the three roles: Architect, Engineer or User.

At creation time, three dimensions are selected:

- **Assignment form:** Tool, Interface, Process or Data.
- **Shaping function:** Builder, Packager, Admin or Dispatch.
- **Role and workspace:** determines the destination and ownership of the work.

These dimensions form a configurable assignment tuple held in a dynamic data structure. New assignment forms and functions can be introduced without redesigning the underlying mechanism.

Activation loads the existing directory structure for the selected role, allows an existing destination to be selected or a new one created, and generates an appropriate placeholder file.

Currently supported placeholder formats are HTML, JSON, Markdown and Python.

Each creation receives a Genesis record containing its origin and intended purpose. The resulting file is ready to evolve: an HTML file can display its own creation record, while JSON can provide structured input for subsequent worker processes.

Every creation is also injected into the relevant role's evolution telemetry, preserving an audit trail of what was created, where, why and for whom.

The entire administration process takes less than a minute.

**Activation makes intent actionable, gives new work an identity and purpose, and records its beginning automatically.**
