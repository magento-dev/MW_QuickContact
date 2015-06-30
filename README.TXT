==== FREE QUICK CONTACT ===

Quick Contact allow customers send the feadback to your site in easiest and fastest way.

PRODUCT FEATURES
----------------

   1. Easy to use for both customers and shop owner
   2. Easy to manage with backend management
   3. Easy to customize with separated form and CSS
   4. Allow user to enable/disable some field like Phone, Subject, Contact Type
   5. Allow user to create new contact type such as Contact, Quote, Question...
   6. Allow user to define received email for each contact type
   7. Allow to enable captcha for guest that protect your site from spam
   8. Allow to enable dock link or add custom link any where
   9. Easy to install, easy to upgrade, just copy to use


INSTALLATION GUIDE
------------------

1. Copy all folders in installation package to magento root folder.

2. Go to Admin / Configuration / Hello Magento / Quick Contact to manage the options.

3. Add this code: <a href="#dialog" name="modal">Quick Contact</a> to anywhere that you want to display the Quick Contact link.

4. You can enable dock link in admin backend instead of add custom link.

3. Go to frontend, refresh page to see how it work.


TRANSLATE MULTIPLE LANGUAGES
----------------------------
Copy this file to other language package and translate it: <magento_root>\app\locale\en_US\HM_QuickContact.csv 


CUSTOM CONTACT FIELDS
---------------------

1. Edit file: app\design\frontend\default\default\template\quickcontact\form.phtml
	................
	<div class="text"> 
		<div class="info-txt"> <?php echo Mage::helper('quickcontact')->__('Your Name')?> <span style="color:#ff0000;">*</span></div>
		<div class="info-txt"> <?php echo Mage::helper('quickcontact')->__('Your Email')?> <span style="color:#ff0000;">*</span></div>
		<div class="info-txt"> <?php echo Mage::helper('quickcontact')->__('Your Phone')?> </div>
		<div class="info-txt"> <?php echo Mage::helper('quickcontact')->__('Your New Field Label')?> </div>
	</div>
	...............
	...............
	<div class="input">
		<input class="input-text textbox" value="<?php if(Mage::helper('customer')->isLoggedIn()) echo Mage::getSingleton('customer/session', array('name'=>'frontend'))->getCustomer()->getName()?>" type="text" name="name" id="name"/>
		<input class="input-text textbox" value="<?php if(Mage::helper('customer')->isLoggedIn()) echo Mage::getSingleton('customer/session', array('name'=>'frontend'))->getCustomer()->getEmail()?>" type="text" name="email" id="email"/>
		<input class="input-text textbox" type="text" name="phone" id="phone" value=""/>
		<input class="input-text textbox" type="text" name="new_field" id="new_field" value=""/>		
	</div>
	..............
	
2. Edit email template file: app\locale\en_US\template\email\quickcontact_form.html
	Name: {{var data.name}}
	E-mail: {{var data.email}}
	New Field: {{var data.new_field}}
	.....................


If you have any problem please email to: support@mage-world.com

Thanks,
Mage-World.com
