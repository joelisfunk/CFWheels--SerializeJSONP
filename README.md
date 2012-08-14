CFWheels--SerializeJSONP
========================

Provides a new function serializeJSONP(data,callback) as well as updates the CFWheels provides() and renderWith() functions to support format 'jsonp'

Usage Example:

&lt;cfcomponent extends="Controller" hint="your custom cfwheels controller"&gt;
	&lt;cffunction name="init"&gt;
		&lt;cfset provides("jsonp")&gt;
	&lt;/cffunction&gt;
	&lt;cffunction name="locations" hint="JSONP requires that you pass a value for variable params.callback"&gt;
		&lt;cfset locations = model("locations").findAll(returnAs="object")&gt;
		&lt;cfset renderWith(locations)&gt;
	&lt;/cffunction&gt;
&lt;/cfcomponent&gt;