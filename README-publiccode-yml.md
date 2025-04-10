# Publiccode.yml

The data for the projects in this repository is maintained following the [publiccode.yml](https://yml.publiccode.tools/) standard. Each project is represented by a YAML file which contains the information about the respective project in a structured form.

## Railway specific extensions

We use the full standard and all but the deprecated fields are allowed.

The scope field, if used, will in most cases be set to `transportation`.

We are adding a new key "businessCapabilities", which reflects which part of the railway business the software targets. This is not an official extension of the standard, yet, but we will make an attempt to evolve the standard to allow for this type of extension.

The businessCapabilities key works as shown in the example below:

    businessCapabilities:
        profile: railway
        cpabilities:
          - sales

The `profile` field is always set to `railway`. It defines which vocabulary can be used in the list of `capabilities`. This would allow to also add specific sets of capabilities for other industry sectors.

For the `railway` sector the following list of values is allowed:

````
Plan Passenger Trip
Inform passenger in real time
Inform Freight Customer
Short-term Staff Disptaching
Short-term Rolling Stock Disptaching
Drive train
Inspect ticket
Care For Passengers
Care For Goods
Manage Emergency
Monitor and control Train Path
Monitor Rolling Stock
Sell Freight Transport
Sell Passenger Transport
Forecast Traffic
Define Price Policy
Provide Rail Network
Provide Passenger Facilities
Provide Freight Facilities
Provide Energy Supply
Provide Data Network
Plan Long Term
Plan Short Term
Sell Network Capacity
Manage Yard
Roster Rolling Stock
Manage Fleet planing
Maintain Rolling stock
Procure Rolling Stock
Manufacture Rolling Stock
Roster Staff
Plan Personal capacities
Recrute and Train Employees
Provide Application Services
Provide Data Center Services
Manage IT-Security
Manage Corporate
Manage Human Ressources
Manage Finance and Controlling
Manage Compliance and Legal Affairs
Manage Supply Chain Management
````

A project can have one or more of these capabilities assigned.

We will add higher-level categories to group these capabilities. These will be used for display of overviews of projects and as additional information to understand the scope of the capabilities. They will not be used as values in specific publiccode.yml files.
