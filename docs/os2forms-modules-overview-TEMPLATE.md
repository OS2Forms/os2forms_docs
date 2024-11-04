# OS2Forms Modules Overview - TEMPLATE

| Customer  | Drupal Version | OS2Forms Version | Upstream Drupal Modules | Os2forms-core Modules                                      | os2forms-contrib Modules      | Custom Modules                                               | Notes |
| --------- | -------------- | ---------------- | ----------------------- | ---------------------------------------------------------- | ----------------------------- | ------------------------------------------------------------ | ----- |
| Customer1 | [Drupal Ver]   | [OS2Forms Ver]   | [Module List]           | [Module1] [Module version]🟢, [Module2] [Module version]🟢 |                               | [Custom1] [Module version]🟡                                 |       |
| Customer2 | [Drupal Ver]   | [OS2Forms Ver]   | [Module List]           | [Module1][Module version] 🟢, [Module2][Module version] 🟢 |                               | -                                                            |       |
| Customer3 | [Drupal Ver]   | [OS2Forms Ver]   | [Module List]           | [Module1] [Module version]🟢, [Module2] [Module version]🟢 | [Contrib1] [Module version]🟡 | [Custom2] [Module version] 🟢, [Contrib1] [Module version]🔵 |       |
| Customer4 | [Drupal Ver]   | [OS2Forms Ver]   | [Module List]           | [Module1] [Module version]🟢, [Module2] [Module version]🟢 |                               | -                                                            |       |
| Customer5 | [Drupal Ver]   | [OS2Forms Ver]   | [Module List]           | [Module1] [Module version]🟢, [Module2][Module version] 🟢 | [Contrib2] [Module version]🔵 | [Custom3] [Module version]❌                                 |       |

## Legend

🟢 : Module is accepted for inclusion
🟡 : Under consideration for removal
🔵 : Under consideration for inclusion
❌ : To be removed

## Template Structure

The template consists of a table with the following columns:

- **Customer**: The name or identifier of the customer.
- **Drupal Version**: The version of Drupal being used.
- **OS2Forms Version**: The version of the OS2Forms distribution.
- **Drupal Core Modules**: A list of core Drupal modules included in the deployment.
- **Os2forms-core Modules**: A list of modules that are part of the os2forms-core distribution, along with their statuses.
- **os2forms-contrib Modules**: A list of contributed modules used in the deployment, along with their statuses.
- **Custom Modules**: Any custom modules developed for the specific deployment, along with their statuses.
- **Notes**: Any additional notes or comments relevant to the deployment.

### Module Types Seperation Suggestions

1. **Core (Os2forms-core Modules)**:
   These are modules used by all members of the OS2Forms community or modules that will be useful for most members in the near future. They form the essential foundation of the OS2Forms distribution. They are located in the main os2forms organisation in the os2forms repository
2. **Contributions (os2forms-contrib Modules)**:
   These are OS2Forms-specific modules that have been developed with funding from a few community members. While not yet considered essential for all member-organizations, these modules are valuable enough that their funders are willing to pay for maintenance. They can be used without modifications in OS2Forms by multiple member-organizations but are not (yet) part of the core distribution. These modules can be located in a seperate repository in the os2forms organisation. The repo could be named "os2forms-module-contributions" to make it clear and easy to understand what is located in the repo.
3. **Custom Modules**:
   These are modules used by only one or two member-organizations, possibly including member-organizations not part of the OS2Forms community. They have not yet been evaluated or considered valuable enough to be part of the contributions-modules. Development and maintenance are outside the control of the OS2Forms community and may require further development before they can be considered for inclusion in the contributions. They are located outside the os2forms organisation, maybe hosted in a development partners git repos or in the
4. **Upstream (Drupal Core Modules)**:
   These are standard Drupal modules used across various member-organizations, both within and outside the OS2 community. OS2 recommends establishing a willingness to contribute to upstream maintenance if an OS2 provider has the opportunity to do so. This ensures the sustainability and improvement of the broader Drupal ecosystem that OS2Forms relies upon.

This structure allows for a clear differentiation between modules that are essential to the OS2Forms distribution, those that are valuable but not universally used, custom solutions for specific needs, and the core Drupal modules that form the foundation of the system.

## How to Fill Out the Template

1. **Customer**: Enter the name or identifier for each customer in the "Customer" column.
2. **Drupal Version**: Specify the version of Drupal that is being used for that customer's deployment.
3. **OS2Forms Version**: Indicate the version of the OS2Forms distribution in use.
4. **Upstream Drupal Core Modules**: List all core Drupal modules that are part of this deployment. You can separate multiple modules with commas.
5. **Os2forms-core Modules**: List all os2forms-core modules being used, followed by their status indicated by one of the icons from the legend. For example:

   - `webform: 6.2.0 🟢`
   - `pathauto: 1.11.0 🟡`
6. **os2forms-contrib Modules**: If there are any contributed modules, list them here along with their version and status.
7. **Custom Modules**: Document any custom modules developed specifically for this deployment, including their status.
8. **Notes**: Use this column to add any relevant comments or additional information about the deployment.

## Example Entry

Here’s an example entry filled out based on the template:

| Customer  | Drupal Version | OS2Forms Version | Drupal Core Modules | Os2forms-core Modules                  | os2forms-contrib Modules | Custom Modules            | Notes        |
| --------- | -------------- | ---------------- | ------------------- | -------------------------------------- | ------------------------ | ------------------------- | ------------ |
| Customer1 | 10.1.3         | 3.0.4            | node, user, system  | webform: 6.2.0 🟢, pathauto: 1.11.0 🟡 | media: 3.0.0 🔵          | custom_module_1: 1.0.0 ❌ | Needs review |
