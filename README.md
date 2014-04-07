Axia ePay PHP Library v1.6.12
=================================
Copyright 2013 Axia ePay, Inc.

[http://secure.axiaepay.com](http://secure.axiaepay.com)

[http://wiki.axiaepay.com/developer/phplibrary](http://wiki.axiaepay.com/developer/phplibrary)

SYNOPSIS
--------
The Axia ePay PHP library is a class for running transactions on the Axia ePay
gateway.  Its feature set roughly follows the [transaction api](http://wiki.axiaepay.com/developer/transaction).  If
you are looking for more features, take a look at [soap api](http://wiki.axiaepay.com/developer/soap/).

SUPPORT
-------
If you have any questions on the use of this library, please contact
the developer integration support department:
   devsupport@axiaepay.com
   866-872-3729 x706
   
For more documentation on using the library, please see
http://wiki.axiaepay.com/developer/phplibrary



REQUIREMENTS
------------
-PHP 4.3.x or higher (http://www.php.net) 

-HTTPs streams support in PHP
or
-Curl/ssl module installed (http://curl.haxx.se/) 


VERIFYING INSTALLATION
----------------------

This package includes a test script "verify_install.php"  that can be used to verify
that your PHP installation is capable of using this library.  Make sure to modify the script
to include the correct path to the library.  Then place the script in web accessable directiory
and access it from a web browser.  If any problems are detected,  follow the on screen 
instructions.


QUICK START
--------------------

	<?php
	include "axiaepay.php";
	$tran=new umTransaction;
	$tran->key="AAAAABBBBBBCCCCCCDDDDDDEEEEEEEE";  
	$tran->card="4444555566667779";	
	$tran->exp="1214";
	$tran->amount="5.00";
	if($tran->process())
	{
		echo "Transaction Approved!";
	} else {
		echo "Transaction Failed: " . $tran->error;
	}
