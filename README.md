<details> <summary>Test cases</summary>
  
 ## Positive Test cases
  1) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Portland, OR
  
     Then patient select illness/injury from drop down menu
  
     And patient select today's date June 23
  
     Then patient select Clinic Care
  
     Verify that user should be able to see the list of doctors with adress information and options for schedruling time.
  
  
  2) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Seattle, WA
  
     Then patient select illness/injury from drop down menu
     
     And patient click on the VideoCare
  
     Then patient select date June 24
  
     Verify that patient should be able to see the list of doctors address information and the time options for appointment 
    

  3) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Vienna, VA
  
     Then verify thta patient should see the message "We're not in your area yet—but we're growing almost as fast as we deliver care! Follow us on social to stay up-to-date on ZoomCare news, announcements and more. Want to see clinics outside of your region? Click below."
  
  4) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Salem, OR
  
     Then patient select illness/injury from drop down menu
      
     And patient select available date from calendar 
  
     Then patient click View Clinic Servises 
  
     And patient should be able to see the list of Services available at this clinic
  
   5) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Denver, CO
  
     Then patient select illness/injury from drop down menu
      
     And patient select available date from calendar 
  
     Then patient click View Clinic Servises 
  
     And patient should be able to see the list of Services available at this clinic
  
     Then patient click on the See More Details
  
     And verify that patient is able to see the list of cervices, doctors name and available time for making an appointment 
  
   6) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Boise, ID
      
     Then patient select Adult Covid-19 Screening
  
     Verify that patient doesn't have option Clinic Care and Chat Care
  
  7) Given patient Log in to ZoomCare or on Schedule ZoomCare
      When patient click on Info | $
      Then patient should be able to see a modal window with information about health           insurance and estimated cost
  
  note: Modal window should be dismissed by clicking on any area outside of modal window, so user experience will improve. Currently you able to close it only when you click again on Info | $ button.
  
  8) Given patient Log in to ZoomCare or on Schedule ZoomCare page
    When patient select family medicine from drop down menu
    And patient select available date from calendar
    Then patient should be able to see the list of services available at this clinic on that particular day
     
     
  
  
  ## Negative Test cases 
  
  1) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Portland, OR
  
     Then patient select illness/injury from drop down menu
  
     And patient try to select past date June 20
  
     Verify that the past date is in read only mode
  
 
  
  
     
     


<details> <summary>Automation Instructions</summary>
  
