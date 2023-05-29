# Validate the Cisco DNAC Site Hierarchy and Inventory 

Open Cisco DNAC using the bookmark in the Chrome browser on your jump host. Log in using the credentials provided by your proctor.

Click the Hamburger Menu and then go to Design->Network Hierarchy.

![DNAC Design Menu](assets/design.png)

On the left-hand side of the screen, you should see an areas. Click the arrow next to the area names to expand them and view your building and floor.

![DNAC Site Hierarchy](assets/site_hierarchy.png)

Next, validate that your network devices were successfully added to the inventory and assigned to your floor. Select the hamburger menu and navigate to `Provision > Inventory`.

![DNAC Provision Menu](assets/provision.png)

This view shows all devices in the Cisco DNA Center inventory. To view your devices, click `Global` in the upper left section of the window next to the hamburger menu select in turn each layer of the hierarchy.

![DNAC Filter Inventory](assets/site_filter.png)

This action filters the inventory to only devices assigned to the site you created. You should see your wan, and access and wireless conrollers within the devices listed. Each in their own part of the hierarchy 

![DNAC Inventory](assets/inventory.png)

It takes time for Cisco DNA Center to finish adding devices to the inventory and collecting details. Your devices may not have the same status at the time you view them, but after a few minutes, Cisco DNA Center will begin to provide Assurance data for these devices.

> [**Next Section**](08-summary.md)


