## About:

Associated Press formatted date/time Caché Server Page RULE for DTI's Content Publisher system.

More information about the AP style guidelines:

* [mah_apstylee](https://github.com/mhulse/mah_apstylee) (PHP/ExpressionEngine version of this code)
* [AP Stylebook](http://www.apstylebook.com/)

If you imporve upon this code and/or have feedback, __please__ contact me: m@mky.io

## Basic usage:

    <custom:rg:apdatetime timestamp="#(ts)#" />

See apdt.csp for more usage examples.

## Non DTI customers:

If you don't use DTI software, but you still want to use this code, then all you have to do is remove these lines of code:

    <csr:class super="dt.common.page.Rule" />

    <script language="cache" runat="compiler">
    	do ..RenderDTStartTag()
    </script>

    <script language="cache" runat="compiler">
    	do ..RenderDTEndTag()
    </script>

## Rule parameters:

* __"timestamp"__ Required. $horolog or ODBC timestamp format.
* __"return"__ What bits of the date do you want returned? Valid choices are 'timeonly', 'dateonly', 'time', 'meridiem', 'day', 'month' and 'year'. Default is the full date and time.
* __"year"__ Set to 'yes' if you want the current year returned. Default is to not return the current year.
* __"today"__ Set to the text you want to return if the day is today. Default is the day number.
* __"noon"__ Set to the the text you want to return if the time is noon. Default is 12.
* __"midnight"__ Set to the text you want to return if the time is midnight. Default is 12.
* __"var"__ Advanced: Name of local variable to use when using as a wrapping tag. Variable name MUST BE UNIQUE!

-----

## Changelog:

* __2011/03/30__
	* Initial public release: Uploaded to GitHub.
