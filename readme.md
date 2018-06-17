<h2>ZN Framework Email Package</h2>
<p>
Follow the steps below for installation and use.
</p>

<h3>Installation</h3>
<p>
You only need to run the following code for the installation.
</p>

```
composer require znframework/package-email
```

<h3>Documentation</h3>
<p>
Click for <a href="https://docs.znframework.com/uzak-servisler/mail-kutuphanesi">documentation</a> of your library.
</p>

<h3>Example Usage</h3>
<p>
Basic level usage is shown below.
</p>

```php
<?php require 'vendor/autoload.php';

ZN\ZN::run();

# The default settings are in the ZN\Email\EmailDefaultConfiguration file. 
Email::smtpHost('mail.example.com')
     ->smtpUser('example@example.com')
     ->smtpPassword('Example1234')
     ->smtpPort(587)
     ->smtpEncode('tls')
     ->from('from@example.com')
     ->to('to@example.com')
     ->send('This is Subject', 'This is message.');

Output::display(Email::error());
```
