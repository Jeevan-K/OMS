({
    doInit: function(component, event, helper) {
		// Find the component whose aura:id is "flowData"
        //var flow = component.find("flowData");
        // In that component, start your flow. Reference the flow's API Name.
        //flow.startFlow("Create_Contact");
        
        
    },
    
    handleSuccess: function(component, event, helper) {
        var newOrder = event.getParams().response;
        var navId = newOrder.id;
        console.log(navId);
        var toastEvent = $A.get("e.force:showToast");
            toastEvent.setParams({
                "type":"success",
                "title": "Saved",
                "mode":"pester",
                "message": "The Order has been created successfully."
            });
            toastEvent.fire();
            
        var navEvt = $A.get("e.force:navigateToSObject");
            navEvt.setParams({
                "recordId": navId 
            });
            navEvt.fire();
   
    }
})
