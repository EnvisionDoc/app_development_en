# Configuring Config Maps and Secrets

This topic describes how application developers can create new config maps and secrets to inject configuration information into the container.

Config maps can be used to store the fine-grained information such as a single attribute, or the coarse-grained information such as an entire profile or a JSON object. The config map can store key/value pair configuration data that can be used in pods. With config maps, it is easier to process strings that do not contain sensitive information.

Secrets are helpful for addressing the configuration of sensitive data such as passwords, tokens and keys without exposing these sensitive data to images or pod specs. A secret can be used as a Volume or as an environment variable. With secrets, it is easier to process strings that contain sensitive information.

## Creating Config Map

You can create a new Config Map for your application as per the following steps:

1. In the left navigation bar, select **Container > Config Maps**.

2. Click the **New Config Map** button and complete the detailed configuration of the config map.

3. Provide basic information about the config map:

   - **Application**: Select an application that requires the config map.
   - **Environment**: Select the config map usage environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.

4. Enter the Config Map information (KEY/VALUE pair) that needs to be configured.

  .. image:: ../../media/config_map.png

5. Enter the description for the config map.

6. Click the **New Config Map** button to complete the configuration.

## Creating Secret

You can create a new secret for your application as per the following steps:

1. In the left navigation bar, select **Container > Secrets**.

2. Click the **New Secret** button and complete the detailed configuration of the secret.

3. Provide the basic information for the secret:

   - **Application**: Select an application that requires the secret.
   - **Environment**: Select the secret usage environment, for which dev, alpha, beta, ppe, and prod environments are supported currently.
   - **Cluster**: Select the cluster where the application is deployed. Note that the cluster is already pre-configured by the system.

4. Select the secret encryption type:

   - **Opaque**: Secret in Base64 encoding format for storing passwords, keys, etc. 
   
     .. note:: The value of the Opaque type needs to be filled with Base64-encrypted content. You can use the online encryption and decryption tool: <http://tool.oschina.net/encrypt?type=3>.

   - **kubernetes.io/rbd**：

     .. image:: ../../media/secret.png

5. Enter the description for the secret.

6. Click the **New Secret** button to complete the configuration.

## Next Step

After the config map and secret are created, you can clone, edit and delete them as needed. The specific steps are similar to those for [Configuring Deployments](configuring_deployment).

<!--end-->
