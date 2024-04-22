# AWS Elastic Beanstalk Sample App with ElastiCache
This sample application uses the [Express](https://expressjs.com/) framework and [ElastiCache](https://aws.amazon.com/elasticache/) to build a performant web application with clustering. This application tracks page views in a session.

This source bundle can be deployed to Elastic Beanstalk using the following steps:
  1. [Install the AWS Elastic Beanstalk Command Line Interface (CLI)](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html).
  2. Run `eb init --platform node.js --region <region>` inside of the `nodejs-example-express-elasticache` directory to initialize the folder for use with the CLI. Replace `<region>` with a region identifier such as `us-east-2` (see [Regions and Endpoints](https://docs.amazonaws.cn/en_us/general/latest/gr/rande.html#elasticbeanstalk_region) for a full list of region identifiers). 
  3. Run `eb create --sample nodejs-example-express-elasticache` to deploy a sample application that contains a load-balanced environment with the default settings for the Node.js platform
  4. Once the environment creation process completes, run `eb open` to load the sample environment in your browser to verify the deployment has succeeded and is accessible.
  5. Deploy the source in this bundle using `eb deploy`.
  6. Once the deployment of this source bundle completes, refresh the page to interact with the new webpage. Each refresh of the page will update the page view count; the page view count can be reset with a hard refresh in your browser.
  7. Run `eb terminate --all` to clean up.

This source bundle can be ran locally using the following steps:
  1. Install Node to your machine, if you haven't already. You can download node from nodejs.org [here](https://nodejs.org/en/). Confirm you have `npm` installed by running `npm -v`. 
  2. Run `npm install` inside of the `nodejs-example-express-elasticache` directory.
  3. Run `npm start`.
  4. Visit the website running locally on your machine at [http://localhost:3000/](http://localhost:3000/)