## How to Roll Out Machine Learning Services using Amazon SageMaker

by Luigi Patruno, Founder of [MLinProduction.com](https://mlinproduction.com/)

TODO [Recorded AWS Webinar](TODO)

## Outline

1. Deployment Strategies for Machine Learning Services
    1. Single Deployment
    2. Silent Intelligence
    3. Controlled Rollout
    4. Flighting
2. Setup
    1. Upload necessary datasets to S3 bucket.
    2. Train multiple predictive models.
    3. Deply models as persistent API endpoints.
    4. View `Endpoint` and `EndpointConfig` details.
3. Blue Green Deployment
    1. Create an Endpoint with a single Production Variant.
    2. Create a new endpoint configuration, using the same production variants for the existing live model and for the new model.
    3. Update the existing live endpoint with the new endpoint configuration. Amazon SageMaker creates the required infrastructure for the new production variant and updates the weights without any downtime.
    4. Switch traffic to the new model through an API call.
    5. Create a new endpoint configuration with only the new production variant and apply it to the endpoint.
4. Canary Deployment
    1. Create an Endpoint with a single Production Variant.
    2. Update the existing live endpoint with the new endpoint configuration. Amazon SageMaker creates the required infrastructure for the new production variant and updates the weights without any downtime.
    3. Gradually move traffic from one variant to the other.
    4. Create a new endpoint configuration with only the new production variant and apply it to the endpoint.
5. References

## If you want to learn how to use Amazon SageMaker for your production ML workloads, [enroll in my new course](https://mlinproduction.teachable.com/p/build-deploy-and-monitor-ml-models-with-amazon-sagemaker)!

![course banner](./figures/course-banner.png)