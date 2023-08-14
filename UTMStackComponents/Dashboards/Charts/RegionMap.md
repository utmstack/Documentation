# Region Map

<img alt="dashobard view" src="./../../../Images/Components/Dashboards/regionMap/result.png">

A Region Map visualization is a geographical representation of your data. It provides a way to visualize the distribution of your data across geographical regions based on the IP addresses or geo coordinates in your dataset.

## Configuration Options

Here are the configuration options for creating a Region Map:

### Map options

- **Latitude**: The latitude value for the initial center point of the map.
- **Longitude**: The longitude value for the initial center point of the map.
- **Zoom**: The initial zoom level of the map. Higher values result in a closer view.
- **Control Position**: The position of the zoom control in the map. You can set it to Top Left, Top Right, Bottom Left, or Bottom Right.

### Map tiles

- **Tile**: The label of the map tile.
- **Tile URL**: The URL for fetching the map tiles. Different URLs provide different styles of maps.(openStreetMap by Default)
- **Tile Attribution**: The attribution of the map tiles.

<img alt="dashobard view" src="./../../../Images/Components/Dashboards/regionMap/conf.png">

## Example: Creating a Region Map for O365 AD Successful Login Locations

If you want to track successful Office 365 login activities based on location, the region map visualization can be a great tool. You can use it to create a geo-distribution of successful logins to your Office 365 Active Directory. Here is how you can create such a region map:

**Step 1:** Apply a Filter

Start by adding a filter that selects the events related to successful user logins. Use the field `logx.o365.Operation.keyword`, set the operator to `is`, and the value to `UserLoggedIn`. This will isolate the user login events in your dataset.

**Step 2:** Configure Map Options

Next, configure the map options. Set the `Latitude` and `Longitude` to `0`, and the `Zoom` level to `1`. This sets the default view of your map to display the whole world. You can adjust these settings according to your needs. Set the `Control Position` to `Top left`.

**Step 3:** Create a Bucket Aggregation

Now, you need to create a bucket aggregation that identifies the location based on the client's IP. In the Data Tab, go to `Split Series` bucket , then select the `Terms` aggregation. Use the field `logx.o365.ClientIP.keyword` to classify the data based on the IP addresses. Set `Order by` to `Metric: COUNT (_count)`, and `Order` to `Descending`. For `Size`, set the value to `1000`, which will show the top 1000 locations by count of successful logins. Lastly, use a `Custom label` like `Location` to identify the information.

After following these steps, you can run the region map to see a visual distribution of successful O365 logins by location. This can help you monitor and track user activity across different geographical locations. 

<img alt="dashobard view" src="./../../../Images/Components/Dashboards/regionMap/result.png">

