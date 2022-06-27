<details> <summary>Test cases</summary>
  
 ## Positive Test cases
  1) Given patient Log in to ZoomCare or on Schedule ZoomCare page
  
     When patient select my location Portland, OR
  
     Then patient select illness/injury from drop down menu
  
     And patient select today's date July 23
  
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
  
      Then patient should be able to see a modal window with information about health insurance and estimated cost
  
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
  
 
  </details>
  
     
    


<details> <summary>Automation Instructions</summary>
  Selenium, Java.
  
  1) Open Eclipse 
  
  Create Maven project
 
  
  Java JDK 8
  
  Chrome
  
  Chrome driver
  
  I will use TestRunner to run the script.
  
    // first we need to connect required libraries to work with selelium webdriver
    import org.openqa.selenium.WebDriver;
    import org.openqa.selenium.chrome.ChromeDriver;
    // then we need to create a class 
    public class ZoomCareSchedule {
    public static void main(String[] args) {
  
    // setting the driver executable, define a path to the chromedriver
    System.setProperty("webdriver.chrome.driver", ".\\Driver\\chromedriver.exe");
  
    // now we need to initiate a chromedriver
    WebDriver driver = new ChromeDriver();
  
    // now we need to maximize window of chrome browser
    driver.manage().window().maximize();
  
    // opening a web browser with specific url
    driver.get("http://zoomcare.com/schedule");
  
    
  1. To write an automation code for the test case #1 we will need to locate all webElements and add to page object class
  
  one file with step definitions
  
  public class StepDef ???? {
  
  NOTES:
  
  1st test case:
  
      @Given("^Patient log in to ZoomCare or on Schedule ZoomCare page$")
      public void patient_login_to_ZoomCare_or_on_Schedule_ZoomCare_page() throws Throwable {
      ??? driver.get("http://zoomcare.com/schedule");
  
      }
  
      @when("^a user selects portland and illness$")
      public void a_user_select_portland_illness_june() throws Throwable {
      //click to expand a location list
      WebElement loc = driver.findElement(By.xpath("//*[@id="react-mount-page-    content"]/div/div/div/div[1]/div/div[1]/div/span"));
      loc.click();
      //click on portland
      WebElement p = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[1]/div[3]/div/div"));
      p.click()
  
      }
  
      @then("^patient selects illness injury from the drop menu$)
      public void patient_selects_illness_injury() throws Throwable {
      // click to expand list of services (illness/injury
      WebElement d = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[1]/div/div/div/i"));
      d.click();
      // click on illness_injury
      WebElement ii = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[2]/div/div[2]/div/div/div/div[2]/div/div/div"));
      ii.click();
      // click to expand dates
      WebElement calen = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[3]/div/div/div[2]/div/i"));
      calen.click();
      // click on June 23
      WebElement date = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[3]/div/div[2]/div/div[4]/div[4]/div[5]/div/div"));
      date.click();
  
      }
  
  2nd test case: 
  
       @Given("^Patient log in to ZoomCare or on Schedule ZoomCare page$")
       public void patient_login_to_ZoomCare_or_on_Schedule_ZoomCare_page() throws Throwable {
       ???? driver.get("http://zoomcare.com/schedule");
  
       }
  
       @when("^patient selects seattle$")
       public void patient_selects_seattle() throws Throwable {
        //click to expand a location list
        WebElement loc = driver.findElement(By.xpath("//*[@id="react-mount-page-    content"]/div/div/div/div[1]/div/div[1]/div/span"));
        loc.click();
  
        //click on seattle
        WebElement p = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[1]/div[4]/div/div"));
        p.click()
        
        }
        @then("^patient selects illness injury from the drop menu$)
        public void patient_selects_illness_injury() throws Throwable {
        // click to expand list of services (illness/injury
        WebElement d = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[1]/div/div/div/i"));
        d.click();
        // click on illness_injury
        WebElement ii = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[2]/div/div[2]/div/div/div/div[2]/div/div/div"));
        ii.click();
        // click on the VideoCare
        WebElement vchat = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[2]/div/div[1]/button[2]"));
        
        // click to expand dates
        WebElement calen = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[3]/div/div/div[2]/div/i"));
        calen.click();
        
        // click on June 24
        WebElement datej = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[3]/div/div[2]/div/div[4]/div[4]/div[6]/div/div"));
  
  
  3rd test case:
  
        
         @Given("^Patient log in to ZoomCare or on Schedule ZoomCare page$")
         public void patient_login_to_ZoomCare_or_on_Schedule_ZoomCare_page() throws Throwable {
         ???? driver.get("http://zoomcare.com/schedule");
  
        }
  
         @When("^patient selects my location Vienna, VA$)
         public void patient_selects_vienna() throws Throwable {
         //click to expand a location list
         WebElement loc = driver.findElement(By.xpath("//*[@id="react-mount-page-    content"]/div/div/div/div[1]/div/div[1]/div/span"));
         loc.click();
         // send key Vienna VA USA
         WebElement locat = driver.findElement(By.xpath("//*[@id="react-mount-page-content"]/div/div/div/div[1]/div/div[2]/div[2]/div/div[1]/input"));
        loxat.sendKeys("Vienna VA");
        
         // not sure how select from the suggestion shown
        List<WebElement> autoSuggestions = driver.findElement ???
        for (WebElement suggestions : autoSuggestions) {
            if (suggestions.getText().contains("Vienna VA)) {
                suggestions.click();
                break;
          }
        }
        
        
  
        
        
  
      
      
  
  
        
  
  
  
  
