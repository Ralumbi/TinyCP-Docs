# Features

After the installation you can edit your settings in features. While you are on your personal TinyCP page and logged in you will see 'three cogs', click on it and click on 'Features'. Then you will see the following breadcrumbs:

Here you will find a documentation about each breadcrumb in the 'Features' section

{% tabs %}
{% tab title="FEATURES" %}
In the features section you can install most necessary applications to run a web-, email- and database-server. You can choose between Apache and Nginx as HTTP server and Apache even comes with extra's such as GIT and/or SVN installation out of the box. Apart from these features it offers extra packages such as LXD Linux Containers, Samba \(used to create virtual hard-drives\) and vsFTPd for secure data transfer.

_**Note for System Admins:**_ _You can only use one HTTP server at this time. If you wish to use Nginx as forwarding server to Apache you should set this up yourself and not installing Apache and/or Nginx from this featured auto installations._
{% endtab %}

{% tab title="SUBSCRIPTIONS" %}
In the subscriptions section you can attach your TinyCP installation to your TinyCP account

You can easily do this by clicking on "Attach to account", after you've done that click on "Update key" to make sure everything is perfectly synchronized. 

At this time TinyCP is not using this specifically, as it is free to use.
{% endtab %}

{% tab title="SETTINGS" %}
In the settings section we can change and add certain functionality's

_General:_  
Here you can set an e-mail to receive information about your server.  
You can change the port which will lead you to your Control Panel as described [&gt;here&lt;](https://docs.tinycp.com/tinycp/installation#completed)
{% endtab %}

{% tab title="UPDATE" %}
The update section describes itself as you can "Check for updates" and install the update when there is one available.
{% endtab %}

{% tab title="IMPORT FROM V1/V2" %}
In the IMPORT section you can import an older and/or same version into another installation of your Control Panel. Everything what is on your other server will be transfered to your current TinyCP installation.

_Note: It is best to only IMPORT when you're on a fresh installation of TinyCP!  
It may cause interferences with your currently data when you're using the same names._
{% endtab %}
{% endtabs %}



