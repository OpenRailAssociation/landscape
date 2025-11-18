# Publiccode.yml

The data for the projects in this repository is maintained following the [publiccode.yml](https://yml.publiccode.tools/) standard. Each project is represented by a YAML file which contains the information about the respective project in a structured form.

## Railway specific extensions

We use the full standard and all but the deprecated fields are allowed.

The scope field, if used, will in most cases be set to `transportation`.

We are adding a new key "businessCapabilities", which reflects which part of the railway business the software targets. This is not an official extension of the standard, yet, but we will make an attempt to evolve the standard to allow for this type of extension.

The businessCapabilities key works as shown in the example below:

    businessCapabilities:
        profile: railway
        capabilities:
          - sales/passenger
          - sales/pricing

The `profile` field is always set to `railway`. It defines which vocabulary can be used in the list of `capabilities`. This would allow to also add specific sets of capabilities for other industry sectors.

For the `railway` sector the following list of values is allowed. See [references/openrail-capabilities.csv](references/openrail-capabilities.csv) for the definition of the IDs with explanations:

````
inform-customer/passenger-timetable
inform-customer/trip-planning
inform-customer/realtime-passenger
inform-customer/realtime-freight
inform-customer/route-guidance
operations/staff-dispatch
operations/rolling-stock-dispatch
operations/train-driving
operations/ticket-inspection
operations/passenger-care
operations/goods-care
operations/emergency
operations/path-control
operations/rolling-stock-monitoring
sales/freight
sales/passenger
sales/traffic-forecasting
sales/pricing
infrastructure/rail-network
infrastructure/passenger
infrastructure/freight
infrastructure/energy
infrastructure/data-network
capacity/long-term
capacity/short-term
capacity/sales
capacity/yard
rolling-stock
rolling-stock/roster
rolling-stock/fleet
rolling-stock/maintenance
rolling-stock/procurement
rolling-stock/manufacture
personnel/roster
personnel/planning
personnel/training
it/applications
it/datacenter
it/security
management/corporate
management/hr
management/finance
management/legal
management/supply-chain
management/real-estate
````

A project can have one or more of these capabilities assigned. In the publiccode.yml files, capabilities are referenced using their IDs (e.g., 'inform-customer/trip-planning' or 'operations/train-driving'). The system automatically converts these IDs to their display names when showing the information on the website.

Each of the capability IDs consists of a high-level category and a concrete capability. The higher-level categories are used to group these capabilities. These will be used for display of overviews of projects and as additional information to understand the scope of the capabilities.

When adding capabilities to a publiccode.yml file, always use the full ID path (e.g., 'operations/train-driving' rather than just 'train-driving').
