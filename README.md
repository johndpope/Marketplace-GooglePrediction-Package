[![](https://scdn.rapidapi.com/RapidAPI_banner.png)](https://rapidapi.com/package/GooglePrediction/functions?utm_source=RapidAPIGitHub_GooglePredictionFunctions&utm_medium=button&utm_content=RapidAPI_GitHub)

# GooglePrediction Package
Build and train cloud-based machine learning models.
* Domain: [Google Prediction API](https://cloud.google.com/prediction)
* Credentials: apiKey, apiSecret

## How to get credentials: 
1. Go to the [Google API Console](https://console.developers.google.com/flows/enableapi?apiid=prediction)
2. Create or select a project.
3. Click Continue to enable the API.
4. On the Credentials page, get an API key and API Secret. 

## GooglePrediction.getAccessToken
Get access token

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| Api key obtained from Google
| apiSecret  | credentials| Api secret obtained from Google
| redirectUri| String     | Your redirect Uri
| code       | String     | Code provided by client

## GooglePrediction.revokeAccessToken
revoke access token

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| User access token

## GooglePrediction.refreshAccessToken
Refresh access token

| Field       | Type       | Description
|-------------|------------|----------
| apiKey      | credentials| Api key obtained from Google
| apiSecret   | credentials| Api secret obtained from Google
| refreshToken| String     | refresh token provided in getAccessToken block

## GooglePrediction.predictWithHostedModel
Submit input and request an output against a hosted model.

| Field          | Type  | Description
|----------------|-------|----------
| accessToken    | String| Api key obtained from Google
| projectId      | String| Id of the project
| hostedModelName| String| Name of the hosted model
| csvInstance    | Array | A list of input features, these can be strings or doubles.

## GooglePrediction.trainModel
Train a Prediction API model.

| Field                       | Type  | Description
|-----------------------------|-------|----------
| accessToken                 | String| Api key obtained from Google
| projectId                   | String| Id of the project
| modelId                     | String| Id of the model. If you train a model that already exists in a project, the model will be overwritten.
| sourceModel                 | String| The Id of the model to be copied over.
| storageDataLocation         | String| Google storage location of the training data file.
| storagePMMLLocation         | String| Google storage location of the preprocessing pmml file.
| modelType                   | String| Type of predictive model (CLASSIFICATION or REGRESSION)
| trainingInstancesOutput     | String| The generic output value - could be regression or class label.
| trainingInstancesCsvInstance| Array | The input features for this instance.
| utility                     | Array | A class weighting function, which allows the importance weights for class labels to be specified (Categorical models only).

## GooglePrediction.getModelAnalysisResult
Get analysis of the model and the data the model was trained on.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| modelId    | String| Id of the model.

## GooglePrediction.getModels
List available models.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| maxResults | Number| Maximum number of results to return.
| pageToken  | String| Pagination token.

## GooglePrediction.checkModelTrainingStatus
Check training status of your model.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| modelId    | String| Id of the model.

## GooglePrediction.getTrainedModelsPrediction
Submit model id and request a prediction.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| modelId    | String| Id of the model.
| csvInstance| Array | A list of input features, these can be strings or doubles.

## GooglePrediction.addDataToModel
Add new data to a trained model.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| modelId    | String| Id of the model.
| csvInstance| Array | A list of input features, these can be strings or doubles.

## GooglePrediction.deleteModel
Delete a trained model.

| Field      | Type  | Description
|------------|-------|----------
| accessToken| String| Api key obtained from Google
| projectId  | String| Id of the project
| modelId    | String| Id of the model.
