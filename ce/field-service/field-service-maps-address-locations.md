---
title: "Enable location and map settings in Dynamics 365 Field Service | MicrosoftDocs"
description: Learn all about location and map settings and how to enable them in Dynamics 365 Field Service.
ms.date: 09/08/2022
ms.reviewer: mhart

ms.topic: article
applies_to:
- "Dynamics 365 (online)"
- "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
search.app:
- D365CE
- D365FS
---

# Enable location and map settings in Dynamics 365 Field Service

Locations and maps are important for getting the most value out of Field Service. For example, knowing the location of work orders and resources allows the solution to effectively route the closest technician (resource) to the service request (work order).

Enable location and map settings to perform functions like:

- Easily get directions so technicians can arrive on time for service appointments.
- Attach latitude and longitude values to addresses (geocode).
- See work orders on a map.
- Configuring geofencing.

> [!Important]
> By connecting to a mapping service, you are allowing the system to share your data. Data includes - but is not limited to - addresses and coordinates, with external systems outside of your Microsoft Dynamics 365 environment. ("Mapping service" refers to Bing Maps or other third-party mapping service designated by you or your operating system). This also applies to Government Cloud environments. Your use of the mapping service will also be subject to their separate terms of use. Data imported from such external systems into Microsoft Dynamics 365 are subject to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).

## Connect to maps

Connecting to maps is enabled by default for new environments. For to validate or change the setting, review the following steps.

1. Open the **Resource Scheduling** app.

1. Change to the **Settings** are and go to **Administration** > **Scheduling Parameters**.

   :::image type="content" source="media/quickstart-rs-settings.png" alt-text="Screenshot of Resource Scheduling settings.":::
    
1. Set **Connect to Maps** to **Yes**.

   :::image type="content" source="media/settings-connect-maps.png" alt-text="Screenshot of connect maps set to yes.":::
    
   > [!Note]
   > In Field Service version 8.8.10.44+ the Bing Maps API key is hidden, and is unavailable for end users and external parties.  

1. Select **Save & Close**.

## Enable auto geocoding for addresses

Geocoding is associating a latitude and longitude to an address. It allows dispatchers to locate work orders more effectively than providing only an address.

For more information, see [Turn on auto geocoding to calculate estimated travel time](turn-on-auto-geocoding.md).

## Enable address suggestions

Field service users can quickly enter account service addresses using Bing Maps address recommendations. As you enter an address, the system will make recommendations. Using address suggestions helps ensure accuracy and reduces data entry errors. 

> [!div class="mx-imgBorder"]
> ![Screenshot of a new work order in Field Service, showing address suggestions in a dropdown menu.](./media/workordernewaddress.png)

Address recommendations are also available on the mobile app for technicians with the appropriate security role. 

To enable location recommendations in Field Service, go to **Settings** > **Field Service Settings** > **Other** tab. 

Address recommendations are on the account, work order, and booking forms.

> [!Note]
> By default, the _Field Service - Resource_ security role has read-only privileges and cannot edit addresses.

## Enable Bing Maps (Show Bing Maps on forms)

Enabling maps makes it so dispatchers and technicians can see a map view on work orders, accounts, and other records.

> [!div class="mx-imgBorder"]
> ![Screenshot of work order map.](media/work-order-map.png) 

Bing Maps is enabled by default for new environments. To confirm Bing Maps is enabled - or to disable Bing Maps - go to **Advanced Settings** > **Settings** > **Administration** > **System Settings** > **General tab** 

> [!div class="mx-imgBorder"]
> ![Screenshot of system settings in Field Service, showing the option to enable Bing Maps.](./media/admin-enable-bing-maps-on-forms.png)

For more information on enabling maps for the work order form, see this article on [managing Bing Maps](/dynamics365/customer-engagement/admin/manage-bing-maps-organization).

## Enable booking maps

Booking maps is a feature that allows frontline workers to see their scheduled jobs on a map.

> [!div class="mx-imgBorder"]
> ![Screenshot of bookings on a map in the Field Service mobile app.](./media/mobile-2020-booking-maps.png)

For more information, see this article: [Enable geospatial features in your environment](/powerapps/maker/canvas-apps/geospatial-overview#enable-the-geospatial-features-for-the-environment) 

## Location tracking

Frontline workers often travel to various locations throughout their work day, and it's helpful for schedulers to know where frontline workers are at any given time. Frontline workers using the Field Service (Dynamics 365) mobile app can enable location sharing from the app, allowing schedulers to visualize their location on the schedule board, and also audit a list showing a frontline worker's location history. See the article on [location tracking](mobile-powerapp-location-auditing.md) for more details.

## Geofencing

A geofence is a virtual perimeter around a specific location. Geofencing allows users to draw zones around places of work, customer sites, and secure areas. You can configure the system to trigger various actions when geofences are crossed by a person or an equipped vehicle. See the article on [geofencing](mobile-powerapp-geofence.md) for more details.

## See also

- [Location tracking, sharing, and auditing](mobile-powerapp-location-auditing.md)
- [Geofencing](mobile-powerapp-geofence.md)
