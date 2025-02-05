# Twitch
-------------

## Creating a custom Twitch OAuth application

The step-by-step instructions below follow Twitch's documentation on [Using OAuth 2.0](https://dev.twitch.tv/docs/authentication/) for authentication.


### Create credentials for ngrok

1.  Navigate to the [Twitch developer console](https://dev.twitch.tv/console), sign in, click **Applications** on the left menu, and then click **Register Your Application**.

2. On the **Register Your Application** page, provide a **Name** for your application, enter `https://idp.ngrok.com/oauth2/callback` in the **OAuth Redirect URLs** field, select **Website Integration** in the **Category** selector, and then click **Create**.

    **Note**: Make sure you have two-factor authentication enabled for your Twitch account.

3. On the **Developer Applications** page, click **Manage** for your application.

4. On the application page, click **New Secret**, and make a note of the **Client ID** and **Client Secret** values.
[![](/img/howto/oauth/1-twitch-register.png)](/img/howto/oauth/1-twitch-register.png)


### Update your endpoint configuration

1. Access the [ngrok Dashboard](https://dashboard.ngrok.com/), sign in, create or edit an edge, and click **OAuth** to enable the OAuth configuration.

2. Select **Twitch** in the **Identity Provider** selector, and select **Use my own OAuth application** in the **OAuth Application** field.

    **Note**: Alternatively, you can select **Use an ngrok-managed OAuth application**. If so, there is no need to create an application in the Twitch developer console.

3. Enter the **Client ID** and **Client Secret** values you copied previously in the corresponding fields and then click **Save** to save the edge configuration.

4. Access your application using the link provided by the **Endpoints** URL of your edge.


### Additional application setup information

*   [Authentication](https://dev.twitch.tv/docs/authentication/)
*   [Registering Your App](https://dev.twitch.tv/docs/authentication/register-app/)
