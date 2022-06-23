<details> <summary>Test cases</summary>
  
 ## Positive Test cases
  1) Given patient Log in to ZoomCare or on Schedrul ZoomCare page
  
     When patient select my location Portland, OR
  
     Then patient select illness/injury from drop down menu
  
     And patient select today's date June 23
  
     Then patient select Clinic Care
  
     Verify that user should be able to see the list of doctors with adress information and options for schedruling time.
  
  
  2) Given patient Log in to ZoomCare or on Schedrul ZoomCare page
  
     When patient select my location Seattle, WA
  
     Then patient select illness/injury from drop down menu
     
     And patient click on the VideoCare
  
     Then patient select date June 24
  
     Verify that patient should be able to see the list of doctors address information and the time options for appointment 
     
     
  
     
  
  
  
  
  

  3) Given patient Log in to ZoomCare or on Schedrul ZoomCare page
  
     When patient select my location Vienna, VA
  
     Then verify thta patient should see the message "We're not in your area yet—but we're growing almost as fast as we deliver care! Follow us on social to stay up-to-date on ZoomCare news, announcements and more. Want to see clinics outside of your region? Click below."
  
  
  
  ## Negative Test cases 
  
  1) Given patient Log in to ZoomCare or on Schedrul ZoomCare page
  
     When patient select my location Portland, OR
  
     Then patient select illness/injury from drop down menu
  
     And patient try to select past date June 20
  
     Verify that the past date is in read only mode
  
     
     


<details> <summary>Automation Instructions</summary>
  
