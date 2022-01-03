# Upgrade from the Previous Version

The previous version of Choreo allowed you to create APIs, services and integrations. The current version introduces the concept of creating Choreo projects with components.

This section explains how to migrate the APIs, services, and integrations you created in the previous version as components to the current version.

!!! note
    Only APIs, services, and integrations created before year 2022 can be migrated.

!!! info
    If you want to continue using the previous version, you can access it via `deprecated.choreo.dev`.<br/><br/>To access the APIs, services and integrations you added in the previous version, you can use the same endpoints as before.

To upgrade from the previous version to the current version, follow these steps:

If you want to upgrade from the previous version to the current version, follow these steps:

## Step 1: Migrate your components

To migrate you components:

1. Access Choreo via console.choreo.dev. Enter your current credentials to sign in.

    You will see the following displayed on the Home page.

    <TODO>

2. Click **Migrate** to migrate your components to the current Choreo version.

    !!! tip
        You can continue to continue your work in the Choreo Console while the migration process runs in the background.

- Once the migration process starts, the following message is displayed.

    <TODO>

- Once the migration process is successfully completed, the following message is displayed.

    <TODO>

- If the migration fails completely or results in being partially completed, the following messages are displayed.

    <TODO>

    !!! note
        If any migration failures occurs, contact support@choreo.io.

Once you have successfully migrated the components, you can proceed to deploy them.
        

## Step 2: Deploy the migrated components

The migrated components are added to a project named `""` in the current Choreo version. They are not deployed.

You can deploy them after editing and testing then in the VS Code Editor as follows:

1. Access the current Choreo version via https://console.preview.choreo.dev/.

2. In the Home page, select the **""** project.

    <TODO>

3. Click on a migrated component. It opens in a separate page.

4. Click **Edit with VS Code Online** to open the component configuration in the VS Code Editor.

5. If there are syntax errors in the code, fix them.

    !!! info
        - You can use code suggestions in the editor to correct the errors. If you need additional information, see [Overview of Ballerina Swan Lake Beta4 - Bug Fixes and Breaking Changes](https://github.com/ballerina-platform/ballerina-release/blob/1d3e4514a356e472c1d021dcba531a517fde8967/release-notes/swan-lake-beta4-release-note.md#bug-fixes-and-breaking-changes)
        - If you require our assistance to carry out this step, contact us via support@choreo.io.
   
6. Once you correct all the errors in the code, commit the component configuration as follows:

   1. Click **Sync with Choreo Upstream** (at the bottom of the page), and then click **Sync my changes with Choreo**.

   2. In the left panel, enter a commit message (e.g., `Implement REST API`)and click on the tick.

       ![Commit message](../assets/img/tutorials/rest-api/commit-message.png){.cInlineImage-half}

      Select **Yes** in the message that appears to specify that you need the changes to be staged.

   3. To push the changes to the GitHub repository, click on the GitHub action menu (marked in the image below), and then click **Push**.

       ![Push changes](../assets/img/tutorials/rest-api/git-action-menu.png){.cInlineImage-half}

       Once the changes are successfully pushed to the GitHub repository, the VS Code Editor indicates by displaying the text **In sync with Choreo upstream** for the `service.bal` file.
   
   4. To deploy the component, click on the **Deploy** icon, and then click the **Deploy** button.
   
   5. To test the component, click on the **Test** icon and try out the component using one of the methods provided in that view.
   
   6. If the tests are successful, click the  **Deploy** icon again, and click **Promote** under **Production** to promote the component to production.
   
   7. Inform your customers of the migration and request them to subscribe to your component again via the Developer Portal.

        !!! info
            Once all the consumers have switched to the new API, the Choreo team will restrict access to the previous Choreo version. 

!!! note
    Migration needs to be completed before 1st March 2022.
