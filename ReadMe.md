# Slugify

<?php
require 'vendor/autoload.php';

use Cocur\Slugify\Slugify;

$slugify = new Slugify();
echo $slugify->slugify("Hello World!") . "<br>"; // hello-world

echo $slugify->slugify("Hello World!", "_") . "<br>"; // hello_world

$slugify->addRule("oe", "ö");
echo $slugify->slugify("Heute ist ein schöner Tag") . "<br>"; // hey

$url = new \Agovo\Slugify\MyUrl();
echo $url->slugify("//https.www.example.org", "Das ist ein langer Text");

