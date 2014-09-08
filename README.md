pdani-Apigee
============

Import and Deployment Bundle

To import and deploy use:
mvn apigee-enterprise:install -P{profile-id value as in parent pom} -Dusername=test@user.com -Dpassword=P@55w05d (where {} are place holders for values based on the environment)

Import Bundle

To Import only:
mvn apigee-enterprise:install -P{profile-id value as in parent pom} -Dbuild.option=deploy-inactive -Dusername={user apigee edge login} -Dpassword={user apigee edge login}

Undeploy Bundle

To undeploy:
mvn apigee-enterprise:install -P{profile-id value as in parent pom} -D build.option=undeploy -Dusername={user apigee edge login} -Dpassword={user apigee edge login} (recommended as this works as saving from the UI, which does import and deploy)

Generate Proxy Bundle

To generate proxy zip file with apiproxy folder and artifacts use:
mvn apigee-enterprise:package -P{profile-id value as in parent pom} -Dbuild.option=deploy-inactive -Dusername={user apigee edge login} -Dpassword={user apigee edge login}.
