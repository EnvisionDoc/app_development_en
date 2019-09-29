# Running Pipelines and Checking Results

After being created, the pipeline will run by the configured triggering mode. Based on your business needs, you can manually trigger a pipeline and view the pipeline running status and results.

## Running a Pipeline

You can manually run a pipeline by taking the following steps:

1. In the left navigation bar, select **Development > Pipeline**.

2. In the list of created pipelines, click the name of a pipeline to open its details page.

3. Click the **Run** button, select a code branch, and run the pipeline.

   .. image:: ../../media/run_pipeline.png


## Viewing Running Results

After the pipeline starts running, its running status and results will be displayed in the **Running Result** section.

1. Click on the job name in the pipeline to see the results of each job:

   .. image:: ../../media/pipeline_success_e.png

2. If a pipeline job fails, click the **View Log** button or download the log to find the cause of errors. After editing the pipeline and jobs, rerun the pipeline.

   .. image:: ../../media/pipeline_failure_e.png

When the build job runs successfully, the image tag will be generated automatically. The naming convention of the image tag is as follows:

- master branch: master_{git_project_name} timestamp, repeatable build 
- feature branch: feature_{feature_name} timestamp, repeatable build
- release branch：{release_name}, non-repeatable build

.. note:: The feature branch refers to the branch other than release branch (not starting with release).

## Next Step

After running the pipeline, you can edit, delete the pipeline, rollback the pipeline deployment configuration, and query its running history.

<!--end-->
