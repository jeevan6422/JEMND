# Restoring the Metadata/Data to the Salesforce Org

This article deals with the procedure for recovering the metadata/data to your respective Salesforce Org and provides information about the menu options that are available for restoring information in Vault.

### Procedure <a id="procedure"></a>

1. Login to your Vault account.
2. Click **Restore** from the Vault dashboard page and click on **Restore Now**.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622364977813.png)
3. On the next screen, select your source **Salesforce Org**.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622365041868.png)
4. Next, select the **restore source** and its **configuration** from the drop-down.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622365127050.png)
5. Click **Get Details**.
6. Based on restore source and configuration selection, the configured list will get displayed.
   1. To restore the source as a **backup**, you can select multiple backups for restoration.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622365278875.png)
   2. For **hierarchical backup** and **archival**, you can choose only one from the list.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622365650714.png)![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622365726225.png)Important Note:Restore Source as **nCino features** will be displayed only for Salesforce orgs configured with nCino objects. For detailed nCino restore process, refer to the article: [nCino Restore Process](https://knowledgebase.autorabit.com/apr21/docs/restoring-ncino-features)
7. Click on either **EZ Restore** or **Selective Restore**.

#### EZ Restore <a id="ez-restore"></a>

EZ Restore copies everything from the source to the destination, including new, updated, and existing data.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622366045954.png)

1. Click on **EZ Restore**.
2. When you click on the **EZ Restore** button, you will be taken to the Restore Checklist as shown below.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622366272576.png)
3. After you've gone through the checklist, click on **Got IT** button.
4. Enter the **label** of your choice or leave the default label which was auto-generated.
5. Specify the **batch size** for components to retrieve records. **10K** is the max batch size that you can set per batch. This option is useful in running large jobs that would exceed normal processing limits. As per the Salesforce governor limit, you can deploy or retrieve up to **10,000 files** at once or a max size of **40MB**. Using Batch Size, you can process records in batches to stay within platform limits. If you have a lot of records, processing records through batches are your best solution.
6. Next, you can select the criteria for the restore to get performed:
   1. **Disable Workflows**: On selection, all the workflows of the Salesforce objects will be deactivated, and the data would be transferred from the source to the destination sandbox. Once the restore is completed, workflows will get activated.
   2. **Disable Validation rules**: Validation rules verify that the data a user enters in a record meets the criteria you specify before the user can save the record. On selection, all the validation rules of the Salesforce objects will be deactivated, and the data would be transferred from the source to the destination sandbox. Once the restore is done, validation rules will get activated.
   3. **Enable serial mode for Bulk API**: Serial mode processes batch one at a time, however, it can increase the processing time for a load.
   4. **Disable Relationship Mapping**: On selection, the child objects related to selected objects will not get fetched.
7. The list of metadata and data objects replicated will be displayed for the last time before the restore process begins. You will not have options to select individuals objects as it is a full restore process.
8. Click **Restore Now**.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622366723629.png)

#### Selective Restore <a id="selective-restore"></a>

This option allows you to select specific metadata/data that gets restored only to the target org.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622366770751.png)

1. Click on the **Selective Restore** button.
2. The next screen displays the list of metadata and data objects that will get replicated. From the list of **Metadata** and **Data** type components, the user needs to select the components \(along with its member\) that will get restored.
3. Under the **Metadata** tab, you can choose the metadata members for each metadata type.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367185365.png)![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367322571.png)![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367457365.png)
4. Under the **Data** tab, you have multiple configurations to choose from:![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367527730.png)
   1. **Schema:** The Schema will allow you to view all the corresponding child objects for your selected object. You may notice in the schema view that some of the objects are auto-selected by default and cannot be unchecked. These are the child objects of its parent object which will be restored for sure if its parent object is selected. However, for other objects which are related to the selected object in some other way, you may have the option to choose them manually.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1623319728654.png)![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1623319742240.png)
   2. **Selected Records:** By default, all the records available in the objects will be auto-selected. To select specific records, click on **"All"** under **Selected Records** which will lead you to a popup box where you can select the record. Post selection the summary table should show the number of records selected.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367679369.png)![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367734069.png)
   3. **Selected Fields:** By default, all the fields will be selected for the objects selected. Clicking on **“All”** under the **Selected Fields** column will open a popup window with all the fields listed for the selected objects. You can also use the **search** filter to search for a specific field faster. Here, you can map your source field with the destination field. By default, the destination field should be mapped based on the source field name.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367828901.png)Important Note:

      1. The mandatory fields are auto-selected, and therefore you do not option to disable them. For example, the ID field.
      2. It is mandatory to select at least one field, if no field is selected and you try to proceed further, a warning popup will be displayed stating **“Select at least one field to proceed”**
      3. The fields which were unchecked will have a null value in the record.

      Based on your selection, the restore will happen for only selected fields. Post selection the summary table should show the number of fields selected.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367878063.png)
5. Click on **Trigger Restore**.
6. When you click on the **Trigger Restore** button, you will be taken to the **Restore Checklist** as shown below.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622367955671.png)
7. After you've gone through the checklist, click on **Got IT** button.
8. On the next screen, enter the **label** of your choice or leave the default label which was auto-generated.
9. Specify the **batch size** for components to retrieve records. 10K is the max batch size that you can set per batch. This option is useful in running large jobs that would exceed normal processing limits. As per the Salesforce governor limit, you can deploy or retrieve up to 10,000 files at once or a max size of 40MB. Using Batch Size, you can process records in batches to stay within platform limits. If you have a lot of records, processing records through batches are your best solution.
10. Next, you can select the criteria for the restore to get performed:
    1. **Disable Workflows**: On selection, all the workflows of the Salesforce objects will be deactivated, and the data would be transferred from the source to the destination sandbox. Once the restore is completed, workflows will get activated.
    2. **Disable Validation rules**: Validation rules verify that the data a user enters in a record meets the criteria you specify before the user can save the record. On selection, all the validation rules of the Salesforce objects will be deactivated, and the data would be transferred from the source to the destination sandbox. Once the restore is done, validation rules will get activated.
    3. **Enable serial mode for Bulk API**: Serial mode processes batch one at a time, however, it can increase the processing time for a load.
    4. **Disable Relationship Mapping**: On selection, the child objects related to selected objects will not get fetched.
11. Click **Restore Now**.![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622368054253.png)
12. You'll be taken to the **Restore Summary** screen, which will display the status of the recently triggered restore activity.

### More Information <a id="more-information"></a>

For each restore activity triggered in Vault, you will find the below details:![](https://cdn.document360.io/8711f4e7-c040-4616-aac9-d947f87e4619/Images/Documentation/image-1622369633025.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Label</td>
      <td style="text-align:left">The label name that you have assigned for your restore activity.
        <br />Click on the <b>Label </b>to find the list of successful/failed metadata
        and data members that are part of the restore operation. Also, you have
        the option to <b>Export </b>to save the restored metadata/data info in CSV
        format locally.</td>
    </tr>
    <tr>
      <td style="text-align:left">Backup Info</td>
      <td style="text-align:left">Get a snapshot of your restore operation</td>
    </tr>
    <tr>
      <td style="text-align:left">Date/Time</td>
      <td style="text-align:left">Date and time stamp for your restore operation</td>
    </tr>
    <tr>
      <td style="text-align:left">Duration</td>
      <td style="text-align:left">Total time took to complete the restore operation</td>
    </tr>
    <tr>
      <td style="text-align:left">MetaSuccess</td>
      <td style="text-align:left">Total count of metadata objects that were successfully restored</td>
    </tr>
    <tr>
      <td style="text-align:left">MetaFailure</td>
      <td style="text-align:left">Total count of metadata objects that failed to restore</td>
    </tr>
    <tr>
      <td style="text-align:left">SuccessRecords</td>
      <td style="text-align:left">Total count of data objects that were successfully restored</td>
    </tr>
    <tr>
      <td style="text-align:left">FailedRecords</td>
      <td style="text-align:left">Total count of data objects that failed to restore</td>
    </tr>
    <tr>
      <td style="text-align:left">Status</td>
      <td style="text-align:left">Restore status (success or failed)</td>
    </tr>
    <tr>
      <td style="text-align:left">Actions</td>
      <td style="text-align:left">
        <p>Additional actions:</p>
        <ul>
          <li><b>Restore summary </b>(
            <img src="https://docs.autorabit.com/Vault/2.0/images/drex_replicate_custom_16.png"
            alt/>): View the restore summary report</li>
          <li><b>Log </b>(
            <img src="https://docs.autorabit.com/Vault/2.0/images/drex_replicate_custom_17.png"
            alt/>): Find the log details for your restore operation</li>
          <li><b>Abort </b>(
            <img src="https://docs.autorabit.com/Vault/2.0/images/drex_replicate_custom_18.png"
            alt/>): For an ongoing replicate operation, you can abort the process in between
            using the <b>Abort </b>icon</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

