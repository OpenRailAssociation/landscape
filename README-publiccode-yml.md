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

For the `railway` sector, capabilities are defined using IDs in a hierarchical structure. The main categories (Level 1) and their subcategories (Level 2) are:

inform-customer - Inform Customer
- inform-customer/timetable - Publish Passenger Timetable and Route Information
- inform-customer/trip-planning - Plan Passenger Trip
- inform-customer/realtime-passenger - Inform passenger in real time
- inform-customer/realtime-freight - Inform Freight Customer in real time
- inform-customer/route-guidance - Guide passenger to alternative routes

operations - Perform passenger and freight transport operations
- operations/staff-dispatch - Short-term Staff Dispatching
- operations/rolling-stock-dispatch - Short-term Rolling Stock Dispatching
- operations/train-driving - Drive train
- operations/ticket-inspection - Inspect ticket
- operations/passenger-care - Care For Passengers
- operations/goods-care - Care For Goods
- operations/emergency - Manage Emergency
- operations/path-control - Monitor and control Train Path
- operations/stock-monitoring - Monitor Rolling Stock

sales - Market and Sale Services
- sales/freight - Sell Freight Transport
- sales/passenger - Sell Passenger Transport
- sales/forecasting - Forecast Traffic
- sales/pricing - Define Price and Product Policy

infrastructure - Provide Railway Infrastructure
- infrastructure/rail-network - Provide Rail Network
- infrastructure/passenger - Provide Passenger Facilities
- infrastructure/freight - Provide Freight Facilities
- infrastructure/energy - Provide Energy Supply
- infrastructure/data-network - Provide Data Network

capacity - Manage Network Capacity
- capacity/long-term - Plan Long Term
- capacity/short-term - Plan Short Term
- capacity/sales - Sell Network Capacity
- capacity/yard - Manage Yard

rolling-stock - Provide Rolling Stock
- rolling-stock/roster - Roster Rolling Stock
- rolling-stock/fleet - Manage Fleet Planning
- rolling-stock/maintenance - Maintain Rolling stock
- rolling-stock/procurement - Procure Rolling Stock
- rolling-stock/manufacture - Manufacture Rolling Stock

personnel - Provide Personnel
- personnel/roster - Roster Staff
- personnel/planning - Plan Personal Capacities
- personnel/training - Recruit and Train Employees

it - Provide Information Technology
- it/applications - Provide Application Services
- it/datacenter - Provide Data Center Services
- it/security - Manage IT Security

management - Provide General Management and Administration
- management/corporate - Manage Corporate
- management/hr - Manage Human Resources
````

A project can have one or more of these capabilities assigned. In the publiccode.yml files, capabilities are referenced using their IDs (e.g., 'inform-customer/trip-planning' or 'operations/train-driving'). The system automatically converts these IDs to their display names when showing the information on the website.

The capabilities are organized in a two-level hierarchy:
- Level 1: Main categories (e.g., 'inform-customer', 'operations', 'sales')
- Level 2: Specific capabilities within each category (e.g., 'inform-customer/trip-planning')

When adding capabilities to your publiccode.yml file, always use the full ID path for Level 2 capabilities (e.g., 'operations/train-driving' rather than just 'train-driving').
