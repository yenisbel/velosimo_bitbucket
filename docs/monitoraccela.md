# Introduction

How to use Velosimo to monitor the EDR-Accela Integration.

## Integration Points with Accela Workflow

The EDR-Accela integration is primarily controlled by the Accela workflow. 


### Route to EDR

The first action performed in the integration is routing the Accela record to EDR.  This action is performed on the Accela Workflow Task configured with the Route to EDR status.  To route documents to EDR the document category and document status must be set to a configured category and status for the integration.

![image](https://user-images.githubusercontent.com/7420659/62165400-e3d75e80-b30d-11e9-8412-410409c640be.png)

In the above screenshot this Record has three documents attached that will be routed to EDR.  In this particular configuration the Category of 1st Review and Document Status of Ready to Route are configured for integration.  Any other documents attached will not get routed to EDR other than those in the configured categories and statuses.

To initiate the routing status the configured workflow task with Route to EDR.  Statusing the task will trigger Velosimo to begin the routing process.

![image](https://user-images.githubusercontent.com/7420659/62165447-023d5a00-b30e-11e9-9eec-a2ff2b311ffd.png)

Upon statusing the task in Accela you will see start to see activity on the Velosimo Flow Execution screen at [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).

![image](https://user-images.githubusercontent.com/7420659/62165486-1b460b00-b30e-11e9-9fe8-529cc7fb455c.png)

The screenshot above is an example of the Flow Executions that take place when routing a new record to EPR.  The first flow triggered will be Accela | Get Record and will end with the Accela | Update Document Status flows.  Depending on the number of documents being routed the number of Download Document and Create Document calls will vary.  A successful routing to EPR will show all flows with a Status of completed.

After successful routing all of the documents in Accela will have a status of Routed for Review, which indicates successful routing to EPR by Velosimo.  

![image](https://user-images.githubusercontent.com/7420659/62165539-33b62580-b30e-11e9-9a5a-e7b4a1669065.png)

At this point you can now launch into EPR by clicking the Review link on the document.

![image](https://user-images.githubusercontent.com/7420659/62165665-75df6700-b30e-11e9-948c-9c96f844c760.png)

### Route for Review

The next action performed in the integration is advancing the Accela Workflow forward to the Review tasks.  This action is performed on the Accela Workflow Task configured with the Route for Review status.

![image](https://user-images.githubusercontent.com/7420659/62165705-95768f80-b30e-11e9-9253-577f9ff2771b.png)


Upon statusing the Task with Route for Review the Accela Workflow Review tasks will activate, a subtask will get added to each activated Review task for each document in the review, and a call will be sent to Velosimo to create the corresponding assignments in EPR. \
 \
Upon statusing the task in Accela you will see start to see activity on the Velosimo Flow Execution screen at [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).

![image](https://user-images.githubusercontent.com/7420659/62165834-d8386780-b30e-11e9-8381-4a180efc4e5c.png)

The screenshot above is an example of the Flow Executions that take place when routing a record for review.  The first flow triggered will be Accela | Get Record Workflow and will end with the ePlanSoft | Create Assignment flows.  Depending on the number of documents and review tasks in Accela the number of Create Assignments will vary.  A successful assignment creation in EPR will show a status of completed.

After successful completion the Accela Workflow will have the Review tasks activated with subtasks created under each Review task.

![image](https://user-images.githubusercontent.com/7420659/62165882-f30adc00-b30e-11e9-8db8-145de03102a2.png)

Clicking the Review link on any of the subtasks will open EPR to the assignments screen where you will see one assignment per Accela workflow subtask.

![image](https://user-images.githubusercontent.com/7420659/62165962-251c3e00-b30f-11e9-84c0-40ca359f786c.png)

### Assignment Status Update

While in the Record is in Review assignment status changes made in EPR will be reflected in Accela.  Any time the EPR assignment status is changed a call is made to Velosimo about the EPR assignment status change.  Velosimo will then update the Accela workflow subtask for the assignment with the status from EPR.

![image](https://user-images.githubusercontent.com/7420659/62166010-3c5b2b80-b30f-11e9-962c-c1fa6210ecfb.png)

In this example the assignment status in EPR is being set to Approved by the user.  Upon clicking Save and Update you will see start to see activity on the Velosimo Flow Execution screen at [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).

![image](https://user-images.githubusercontent.com/7420659/62166057-55fc7300-b30f-11e9-908a-497366badb42.png)

One Velosimo flow execution will be performed per EPR assignment status change.  Upon success you will see the status updated on the subtask of the Review task in Accela.

![image](https://user-images.githubusercontent.com/7420659/62166096-6b719d00-b30f-11e9-9aa7-7b175f4f733d.png)

### Corrections Required

Once all of the Review tasks are completed the Accela Workflow will advance to a Review Consolidation task.  In the case of the review needing corrections the Review Consolidation task (or equivalent depending on your configuration) will get statused with Corrections Required.  Upon statusing with Corrections Required an event will be sent to Velosimo to generate the EPR corrections report and get all documents from EPR requirement a revision.

![image](https://user-images.githubusercontent.com/7420659/62166157-8e9c4c80-b30f-11e9-8191-ddd6306c7eed.png)

Documents requiring revisions in EPR are determined by the Assignment status in EPR.  For a document to get detected as needing revisions there must be one or more assignments with the Corrections Required status and all other statuses for the document must be Approved or Approved with Comments.  If a document has one assignment still active (or not in the Corrections Required, Approved, or Approved with Comments status) state the document will not get detected as needing corrections.

![image](https://user-images.githubusercontent.com/7420659/62166205-b095cf00-b30f-11e9-9bc7-8e2beae66f9c.png)

Upon applying the Corrections Required status in Accela you will start to see activity in the Velosimo Flow Executions at [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).

![image](https://user-images.githubusercontent.com/7420659/62166241-c99e8000-b30f-11e9-9210-6731c4dde1ae.png)

The screenshot above is an example of the Flow Executions that take place when statusing with Corrections Required  The first flow triggered will be ePlanSoft | Get Project Documents and will end with the Accela | Update Original Documents flows.  The number of overall flow executions will vary depending on the number of documents coming back from EPR for corrections.

Typical behavior is to see the ePlanSoft | Get Deliverable flow fail and retry 2-5 times.  At this step EPR is building the Deliverable which may take a few moments depending on the size and number of documents coming back from review.  If this flow fails more than 5 times and continues to retry there is an issue with one of the PDFs not printing in EPR.  See the troubleshooting section below for more information on how to troubleshoot this issue.

![image](https://user-images.githubusercontent.com/7420659/62166279-e20e9a80-b30f-11e9-994e-288586f01b51.png)

Upon successful routing of the documents to Accela you will see a set of new documents on the Accela record.  There will be one corrections report and N number of Corrections Required documents added to the Accela.  The number of documents depends on the number needing corrections in EPR.


### Approved

Once all of the Review tasks are completed the Accela Workflow will advance to a Review Consolidation task.  In the case of the all reviews being Approved the Review Consolidation task (or equivalent depending on your configuration) will get status of Approved.  Upon statusing with Approved an event will be sent to Velosimo to get all documents from EPR requirement a revision.

![image](https://user-images.githubusercontent.com/7420659/62166319-fe123c00-b30f-11e9-926d-bcbb30d7f5a8.png)

Approved documents in EPR are determined by the Assignment status in EPR.  For a document to get detected as Approved all assignments for the document must have a status of Approved or Approved with Comments.  If a document has one assignment still active (or not in the Approved or Approved with Comments status) the document will not get detected Approved.

![image](https://user-images.githubusercontent.com/7420659/62166375-226e1880-b310-11e9-8fe9-92888a7e1b0e.png)

Upon applying the Approved status in Accela you will start to see activity in the Velosimo Flow Executions at [https://connect.velosimo.com/flow_execution](https://connect.velosimo.com/flow_execution).

![image](https://user-images.githubusercontent.com/7420659/62166401-31ed6180-b310-11e9-8efa-49b7fb55cf7f.png)

The screenshot above is an example of the Flow Executions that take place when statusing with Approved.  The first flow triggered will be ePlanSoft | Get Project Documents and will end with the Accela | Update Original Documents flows.  The number of overall flow executions will vary depending on the number of documents coming back from EPR.

Typical behavior is to see the ePlanSoft | Get Deliverable flow fail and retry 2-5 times.  At this step EPR is building the Deliverable which may take a few moments depending on the size and number of documents coming back from review.  If this flow fails more than 5 times and continues to retry there is an issue with one of the PDFs not printing in EPR.  See the troubleshooting section below for more information on how to troubleshoot this issue.

![image](https://user-images.githubusercontent.com/7420659/62166419-42054100-b310-11e9-9551-624b6716bcb8.png)

Upon successful routing of the documents to Accela you will see a set of new documents on the Accela record.


### Troubleshooting

#### Deliverables Not Generating

One issue typically encountered at this step is the EPR Deliverable not generating and the Velosimo ePlanSoft | Get Deliverable flow to continue to fail and retry.  In this situation the document cannot be printed in EPR and must be fixed and the deliverable re-generated.  To locate flows that are failing to the Flow Execution page in Velosimo and filter the list by Status=failed and Flow=Get Deliverable.  This will show all of the current failing Get Deliverable flows.

![image](https://user-images.githubusercontent.com/7420659/62166477-62cd9680-b310-11e9-8ddd-c1f5a15d71e5.png)

To correct the issue first stop the auto-retry of the Get Deliverable flow to stop it from continuing to retry.  To turn off auto-rety click the : menu icon and go to Edit on the menu.

![image](https://user-images.githubusercontent.com/7420659/62166544-914b7180-b310-11e9-95ce-4790a852b148.png)

On the Flow Execution Edit screen change the Auto-retry value to manually and click Save.  You can also optional add a note in the Description to help keep tracking of troubleshooting efforts.

![image](https://user-images.githubusercontent.com/7420659/62166611-c3f56a00-b310-11e9-9533-4adf9223c25b.png)

Once saved you go into the information for the Flow Execution by clicking Show on : menu the Flow Executions screen.

![image](https://user-images.githubusercontent.com/7420659/62166639-d40d4980-b310-11e9-851b-31742a1e8ce5.png)

Clicking Show will bring up the details of the Get Deliverable flow execution.  The Accela Record ID will be printed in the Notifications section.

![image](https://user-images.githubusercontent.com/7420659/62166673-ec7d6400-b310-11e9-92e5-8a6003ebedc3.png)

Next lookup the Record in question in EPR and try to generate a deliverable manually from within EPR.  In most cases you will get an error indicating the selected PDF cannot be printed and must be fixed in order to work correctly.

#### Troubleshooting General Failures 

Should a failure occur during routing the Flow Execution screen will show a status of Failed.  To view the details of the Failure click the right : menu on the flow execution and then click Show.

![image](https://user-images.githubusercontent.com/7420659/62166723-0fa81380-b311-11e9-980a-e753b275b0e4.png)

Clicking Show will display the detailed information for that specific execution.  The Notifications section will contain the detailed information about the API call and the response.

![image](https://user-images.githubusercontent.com/7420659/62166759-251d3d80-b311-11e9-91ec-8127a30b0a60.png)

In the example above the API call failed with a response_code 400 indicated by the red text in the notification.  Click the Attachment to see the detailed response from the API. \
 \

![image](https://user-images.githubusercontent.com/7420659/62166794-3bc39480-b311-11e9-9f8a-4c03c8099204.png)

The above is the Attachment for the failure.  At this point contact Velosimo Support using the Velosimo Slack Channel for help troubleshooting this issue should the error not be clear.
