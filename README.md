<?php
require_once __DIR__ . '/config.php';
require_once __DIR__ . '/facebook-sdk/autoload.php';

use Facebook\Facebook;

$facebook = new Facebook([
  'app_id' => APP_ID,
  'app_secret' => APP_SECRET,
  'default_access_token' => null,
]);

$helper = $facebook->getRedirectLoginHelper();


$permissions = ['email', 'public_profile']; // Add more permissions as needed

$loginUrl = $helper->getLoginUrl($permissions);

echo "<a href='$loginUrl'>Log in with Facebook</a>";
?>
$status_url = 'https://www.gfs.tle.com/deletion?id=abc123