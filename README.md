CFWheels--SerializeJSONP
========================

Provides a new function serializeJSONP(data,callback) as well as updates the CFWheels provides() and renderWith() functions to support format 'jsonp'

Usage Example:

<cfcomponent extends="Controller" hint="your custom cfwheels controller">
	<cffunction name="init">
		<cfset provides("jsonp")>
	</cffunction>
	<cffunction name="locations" hint="JSONP requires that you pass a value for variable params.callback">
		<cfset locations = model("locations").findAll(returnAs="object")>
		<cfset renderWith(locations)>
	</cffunction>
</cfcomponent>