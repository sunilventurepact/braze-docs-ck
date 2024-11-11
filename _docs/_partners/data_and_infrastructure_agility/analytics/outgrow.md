---
nav_title: Outgrow
article_title: Outgrow
alias: /partners/outgrow/
description: "This article provides a comprehensive guide on configuring a native integration between Outgrow and Braze for enhanced user data synchronization and personalized campaigns."
page_type: partner
search_tag: Partner
---

# Outgrow

> [Outgrow](https://outgrow.co/), an interactive content platform, enables businesses to create quizzes, calculators, surveys, and other types of engaging content to collect user data and insights. The Braze-Outgrow integration lets you automatically transfer user data from Outgrow into Braze, enabling highly personalized and targeted campaigns.

## Advantages of Using Braze with Outgrow

Integrating Braze with Outgrow provides several benefits for businesses seeking to leverage interactive content for customer engagement:

 **Enhanced Personalization**: Collect data from Outgrow quizzes, surveys, and calculators, which can be mapped to custom attributes in Braze. This data enables precise segmentation and personalized campaigns, improving engagement and conversion rates.

 **Real-time Data Sync**: Outgrow data is sent to Braze in real-time, allowing you to act on user insights immediately. This enables timely follow-ups or personalized messages based on users' most recent interactions.

 **Streamlined Data Management**: The integration automates data transfer between Outgrow and Braze, eliminating manual data exports and imports, reducing data discrepancies, and saving time.

 **Improved User Experience**: Leverage user insights to create more relevant experiences, leading to higher satisfaction, retention, and lifetime value.

 **Flexible Targeting and Segmentation**: Refine segmentation in Braze using Outgrow data, enabling you to target users based on specific interactions, such as quiz scores or survey responses, to create campaigns that resonate with your audience.

## Prerequisites

Before setting up the Outgrow and Braze integration, ensure you have the following:

| Requirement | Description |
|-------------|-------------|
| **Outgrow Account** | A registered Outgrow account to configure and manage interactive content and data transfer settings. |
| **Braze Account** | A Braze account with access to REST API credentials. |
| **API Key** | An API Key from Braze with appropriate permissions (e.g., `users.track`) to enable user data transfer. |
| **Custom Attributes in Braze** | Custom attributes set up in Braze to capture Outgrow responses (e.g., quiz scores, segments). |
{: .reset-td-br-1 .reset-td-br-2}

## Integration Setup

Follow these steps to configure the Outgrow-Braze integration:

### Step 1: Generate Braze API Key

1. In your Braze account, go to **Developer Console > API Settings**.
2. Select **Create New API Key**.
3. Name your API key, enable the `users.track` permission, and save the API key securely.

### Step 2: Configure the Braze Integration in Outgrow

1. Log into your Outgrow account.
2. Navigate to **Integrations** in the dashboard.
3. From the list of available integrations, select **Braze**.
4. Enter your **Braze API Key** and **REST API Endpoint URL**.

   - **API Key**: Paste the API key generated in Braze.
   - **REST Endpoint URL**: Enter the endpoint for your Braze instance (e.g., `https://rest.iad-01.braze.com`).

5. Click **Save** to enable the integration.

### Step 3: Map Outgrow Data to Braze Attributes

In Outgrow, you can map responses from interactive content (such as quiz results, custom segments, or engagement scores) to Braze custom attributes.

1. In the Outgrow **Integration Settings** for Braze, define which Outgrow responses to map to Braze attributes.
2. Ensure that each selected response aligns with a custom attribute in Braze. For example:
   - Quiz score → `outgrow_quiz_score`
   - Custom segment → `outgrow_custom_segment`
3. Save your mapping settings.

### Step 4: Test the Integration

After configuring the integration, run a test to ensure data is properly transferring from Outgrow to Braze.

1. Publish an Outgrow experience (e.g., a quiz or calculator) and complete it as a test user.
2. In your Braze account, go to the **User Profile** section and check for updated attributes (e.g., `outgrow_quiz_score` or `outgrow_custom_segment`).
3. Verify that the data is correctly populated under the appropriate custom attributes.

## Using Outgrow Data in Braze for Segmentation and Targeting

### Creating Segments in Braze with Outgrow Data

With the Outgrow integration, you can create Braze segments based on custom attributes populated from Outgrow responses:

1. In Braze, navigate to **Engagement > Segments** and select **Create New Segment**.
2. Name your segment and set filters based on Outgrow data. For example:
   - Filter by `outgrow_quiz_score` to target users who scored above a certain threshold.
   - Filter by `outgrow_custom_segment` to target users who belong to a particular Outgrow-defined segment.

3. Save your segment for use in campaigns and Canvases.

### Launching Campaigns with Outgrow-Defined Segments

Use the custom segments created from Outgrow data to personalize your Braze campaigns:

1. In Braze, go to **Engagement > Campaigns**.
2. Select **Create Campaign** and choose your campaign type (email, push, in-app message, etc.).
3. In the audience targeting step, select the segment created from Outgrow attributes (e.g., users with specific quiz scores or segments).
4. Customize your campaign content and settings, then launch.

This allows you to target users based on their responses to interactive content, providing a more personalized user experience.

## Troubleshooting Common Issues

| Issue | Solution |
|-------|----------|
| **Data Not Transferring to Braze** | Verify that the API key and endpoint URL are correct in the Outgrow integration settings. Check that the API key has the `users.track` permission enabled. |
| **Incorrect Data Mapping** | Ensure that each mapped Outgrow response corresponds to a valid Braze custom attribute and that attribute names match exactly. |
| **Segment Not Filtering Correctly** | Make sure that custom attributes in Braze are properly set up and receiving data. Re-check your segment filter logic. |

## Additional Considerations

- **Data Privacy**: Ensure compliance with data privacy regulations (e.g., GDPR, CCPA) when transferring user data between platforms.
- **Rate Limits**: Outgrow data is sent to Braze in real-time, but Braze API rate limits may apply for large volumes of data. Plan accordingly for high-traffic experiences.
- **Custom Attribute Configuration**: Ensure that Braze custom attributes used in this integration are correctly configured to capture data sent from Outgrow.

For further assistance, refer to the [Outgrow Documentation](https://support.outgrow.co/docs/configuring-native-integration-between-outgrow-braze) or reach out to Outgrow Support.

---

This setup allows you to seamlessly transfer user data from Outgrow to Braze, enhancing your ability to personalize and target campaigns based on user engagement with interactive content. 
