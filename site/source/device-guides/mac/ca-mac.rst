.. _ca-mac:

============================
Trusting Your Root CA on Mac
============================
Complete this guide to trust your server's Root Certificate Authority (Root CA) on Mac.

#. Ensure you have :ref:`downloaded your Root CA <root-ca-download>`

#. Locate your downloaded Root CA. Right click it and select *Show in Folder*:

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-3-show_in_folder.png
        :width: 60%
        :alt: Show certificate file in Downloads folder

#. Finder will open.  Locate your unique `adjective-noun.crt` file in your *Downloads* folder and double click it to import it into the *Keychain Access* program.  You will be prompted for your macOS username and password, or thumbprint.  Then select *Modify Keychain*:

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-4-modify_keychain.png
        :width: 60%

#. Press Command + Spacebar to launch a program, type in *Keychain Access* and select the resulting *Keychain Access* program to open it.

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-4.5-keychain_access.png
        :width: 60%

#. Your server's CA certificate will be displayed among the imported certificates in Keychain Access.  Right-click on the imported CA cert and select *Get Info*:

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-5-cert-get_info.png
        :width: 60%
        :alt: Keychain Access - Get Info of CA Certificate

#. The details of your CA certificate will be displayed in a new dialog window.  Expand the **Trust** heading, then select "**Always Trust**" on **Secure Sockets Layer (SSL)** and **X.509 Basic Policy**.

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-6-ssl_tls-always_trust.png
        :width: 60%
        :alt: Trust CA Certificate

    Click the red (x) button at the top left of the Local Root CA dialog window.

#. You will then be prompted again for your username and password, or thumbprint.  Enter those and click **Update Settings**:

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-7-password-update_settings.png
        :width: 60%
        :alt: Authenticate to change the settings

#. You will see your server's CA certificate as trusted now, signified by a blue (+) sign and the CA cert information will now say "This certificate is marked as trusted for all users" in Keychain Access:

    .. figure:: /_static/images/ssl/macos/trust-cert-macos-8-cert_trusted.png
        :width: 60%
        :alt: Keychain submenu

    .. tip:: If the keychain console did not show the certificate as trusted, press "Command + spacebar" and type “Keychain Access”, and hit enter to re-open it.

#. From macOS Sequoia (15) onwards, you'll need to allow your preferred browser to find devices on local networks.

    - When you first use software on your Mac that wants to access the local network (either after you upgrade to Sequoia or whenever you run new software you have just installed) you'll be asked whether to allow local network access. Click **Allow**.

        .. figure:: /_static/images/ssl/macos/sequoia-local-access.png
            :width: 20%
            :alt: Sequoia LAN access

    - If you denied access at some point in the past and no longer have this option pop up for you, go to **Settings** then **Privacy & Security** then **Local Network** and finally toggle on the browser(s) you want to use.

        .. figure:: /_static/images/ssl/macos/sequoia-local-access-settings.png
            :width: 60%
            :alt: Sequoia LAN access

#. If using Firefox or Tor Browser, complete :ref:`this final step <ca-ff>`.
