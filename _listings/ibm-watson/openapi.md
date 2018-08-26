---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 1
info:
  title: IBM Watson Machine Learning API
  description: -authorizationstep-by-step-instruction-how-to-use-watson-machine-learning-servicecan-be-found-herehttpsdatascience-ibm-comdocscontentanalyzedatamloverview-htmlcontextanalytics-ibm-watson-machine-learning-credentialsto-start-working-with-api-one-needs-to-generate-an-access-token-using-the-username-and-passwordavailable-on-the-service-credentials-tab-of-the-ibm-watson-machine-learning-service-instance-or-also-available-in-the-vcap-environment-variable-example-of-the-service-credentialsjson----url-httpsibmwatsonml-mybluemix-net----username-c1ef4b802ee2458eab92e9ca97ec657d----password-030528d45a3e4d4c92585d553513be6f----instance-id-a751c209954edc32b441ad56ce7a9f40example-of-obtaining-access-token-from-token-endpoint-using-http-basic-auth-for-details-please-refer-to-token-section-belowcurl-basic-user-usernamepassword-httpsibmwatsonml-mybluemix-netv3identitytokenthe-obtained-access-token-needs-to-be-prepended-with-bearer-word-and-it-needs-to-be-passed-in-the-authorization-header-for-api-calls-example-of-api-request-with-bearer-access-tokencurl-httpsibmwatsonml-mybluemix-netv3wml-instances00fd89e68cf24712a068ade10277b649published-models-h-authorization-bearer-eyjhbgcioijsuzuxmiisinr5cci6ikpxvcj9-eyj0zw5hbnrjzci6imu4ymqzzgm3lwi5y2utndy1oc1iz----apache-spark-service-credentialsthe-ibm-watson-machine-learning-cooperates-with-the-apache-spark-as-a-service-to-create-batch-stream-deploymentsand-for-learning-configuration-functionality-for-api-methods-requiring-apache-spark-service-instance-a-custom-header-xsparkserviceinstancewith-service-credentials-must-be-specified-the-header-value-is-a-base64-encoded-string-with-the-json-data-containing-service-credentials-and-spark-version-example-of-the-json-data---credentials------tenant-ids068ade10277b6495605b1d10fv12b------tenant-id-full00fd89e68cf24712a068ade10277b649-41f37bf21b954c65a15605b1d10fb12b------cluster-master-urlhttpsspark-bluemix-net------instance-id00fd89e68cf24712a068ade10277b649------tenant-secretc74c37cf482a4da4836ef32ca26ccbb9------planibm-sparkservice-paygopersonal------version2-0
  version: 1.0.0
host: ibm-watson-ml.mybluemix.net
basePath: v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /wml_instances/{instance_id}/published_models:
    get:
      summary: Get Wml Instances Instance Published Models
      description: Get wml instances instance published models.
      operationId: listModelDeployments
      x-api-path-slug: wml-instancesinstance-idpublished-models-get
      parameters:
      - in: query
        name: limit
        description: Maximum number of resources to retrive (defaults to 1000)
      - in: query
        name: start
        description: Token required for token-based pagination
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
  /wml_instances/{instance_id}/published_models/{published_model_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model
      description: Get wml instances instance published models published model.
      operationId: details-about-specific-published-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    delete:
      summary: Delete Wml Instances Instance Published Models Published Model
      description: Delete wml instances instance published models published model.
      operationId: deletes-the-published-model-and-all-its-deployments
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-delete
      parameters:
      - in: query
        name: ignore_spark_errors
        description: If this flag is set to true then deployments of this model will
          be deleted even if spark reports failure in response to kill job request
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model
      description: Patch wml instances instance published models published model.
      operationId: updates-the-version-of-deployed-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-patch
      parameters:
      - in: body
        name: published_model_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/evaluation_metrics:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Evaluation
        Metrics
      description: Get wml instances instance published models published model evaluation
        metrics.
      operationId: listModelMetrics
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idevaluation-metrics-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Evaluation
      - Metrics
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_configuration:
    put:
      summary: Put Wml Instances Instance Published Models Published Model Learning
        Configuration
      description: Put wml instances instance published models published model learning
        configuration.
      operationId: creates-learning-configuration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-put
      parameters:
      - in: body
        name: learning_configuration
        description: The model deployment Id
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Configuration
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model Learning
        Configuration
      description: Patch wml instances instance published models published model learning
        configuration.
      operationId: updates-the-learning-configuration-partially
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-patch
      parameters:
      - in: body
        name: learning_configuration_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Configuration
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Learning
        Iterations
      description: Post wml instances instance published models published model learning
        iterations.
      operationId: evaluateModel
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-post
      parameters:
      - in: body
        name: learning_iteration_settings
        description: Settings for this particular learning iteration
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
    get:
      summary: Get Wml Instances Instance Published Models Published Model Learning
        Iterations
      description: Get wml instances instance published models published model learning
        iterations.
      operationId: listModelLearningIterations
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-get
      parameters:
      - in: query
        name: status
        description: This is the filter parameter which allows to query learning iterations
          with the specific status
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations/{learning_iteration_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Learning
        Iterations Learning Iteration
      description: Get wml instances instance published models published model learning
        iterations learning iteration.
      operationId: details-about-specific-learning-iteration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterationslearning-iteration-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Iterations
      - Learning
      - Iteration
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/feedback:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Feedback
      description: |-
        Receives the feedback data and stores it in the feedback store
        defined in learning configuration
      operationId: receives-the-feedback-data-and-stores-it-in-the-feedback-storedefined-in-learning-configuration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idfeedback-post
      parameters:
      - in: body
        name: feedback_data
        description: The feedback data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Feedback
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Deployments
      description: Creates the deployment - online, stream, batch (batch deployment
        only supports Cloud Object Storage as input/output for Tensorflow, Keras and
        Caffe models.)
      operationId: creates-the-deployment--online-stream-batch-batch-deployment-only-supports-cloud-object-storage-as-i
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeployments-post
      parameters:
      - in: body
        name: deployment_input
        description: The input data
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: sync
        description: This is parameter which determines if the online deployment needs
          to be created in synchronous or asynchronous way
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
    get:
      summary: Get Wml Instances Instance Published Models Published Model Deployments
      description: Get wml instances instance published models published model deployments.
      operationId: listDeploymentsForModel
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeployments-get
      parameters:
      - in: query
        name: status
        description: This is the filter parameter which allows to query deployments
          with the specific status
      - in: query
        name: type
        description: This is the filter parameter which allows to query deployments
          with the specific type
      - in: query
        name: _fields
        description: The list of fields which should be included in the response
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Get wml instances instance published models published model deployments
        deployment.
      operationId: getDeployment
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Patch wml instances instance published models published model deployments
        deployment.
      operationId: allows-to-update-the-deployed-stream-status-startstop
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-patch
      parameters:
      - in: body
        name: deployment_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
    delete:
      summary: Delete Wml Instances Instance Published Models Published Model Deployments
        Deployment
      description: Delete wml instances instance published models published model
        deployments deployment.
      operationId: ""
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-delete
      parameters:
      - in: query
        name: ignore_spark_errors
        description: If this flag is set to true then the deployment will be deleted
          even if spark reports failure in response to kill job request
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}/online:
    post:
      summary: Post Wml Instances Instance Published Models Published Model Deployments
        Deployment Online
      description: Post wml instances instance published models published model deployments
        deployment online.
      operationId: makes-an-online-prediction-on-a-given-data-values
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-idonline-post
      parameters:
      - in: body
        name: online_prediction_input
        description: The input data
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Deployments
      - Deployment
      - Id
      - Online
  /wml_instances/{instance_id}/deployments:
    get:
      summary: Get Wml Instances Instance Deployments
      description: Get wml instances instance deployments.
      operationId: listAllDeployments
      x-api-path-slug: wml-instancesinstance-iddeployments-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Deployments
  /wml_instances/{instance_id}:
    get:
      summary: Get Wml Instances Instance
      description: Details about specific service instance
      operationId: getInstanceDetails
      x-api-path-slug: wml-instancesinstance-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
---