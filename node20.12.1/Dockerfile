FROM node:20.12.1-bookworm

WORKDIR /workdir

# Install AWS CLI
# https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install
# Install AWS Amplify
# Install AWS CDK
RUN npm install -g @aws-amplify/cli  aws-cdk

# Install SAM
# https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-linux.html
RUN curl -L "https://github.com/aws/aws-sam-cli/releases/latest/download/aws-sam-cli-linux-x86_64.zip" -o "aws-sam-cli-linux-x86_64.zip" && \
    unzip aws-sam-cli-linux-x86_64.zip -d sam-installation &&  \
    ./sam-installation/install

# Clean Up zips
RUN  rm awscliv2.zip aws-sam-cli-linux-x86_64.zip