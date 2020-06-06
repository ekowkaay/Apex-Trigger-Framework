# Salesforce-Trigger-Framework
<p>A simple easy-to-use trigger handler framework for Salesforce Apex.</p> 

<h1>How to implement this trigger pattern</h1>
<ol>
	<li>Copy the ITriggerHandler and TriggerDispatcher classes into your org (in that order). Or you can use the <em>Deploy To Salesforce</em> link below.</li>
	<li>Create an objectTriggerHandler class (such as OpportunityTriggerHandler), which implements the ITriggerHandler interface. Have a look at the AccountTriggerHandler class in this repository for a working example.
	<li>Add logic for the methods you require. For example, if you want some BeforeInsert logic, add it to the BeforeInsert method in your handler class.</li>
	<li>Create a trigger for your object which fires on all events. If you're using MavensMate/Sublime Text, there is a template for this when you create a new trigger. Take a look at the example AccountTrigger in this repository if you're not sure.</li>
	<li>Call the static TriggerDispatcher.Run method from your trigger. Pass it a new instance of your TriggerHandler class as an argument</li>
	<li>Take a tea break. You've earned it.</li>
</ol>
