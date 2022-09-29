# Leads-Saver

## About

A Lead saver chrome browser extension that can save and then also delete multiple or single URL's from either custom user input or the current chrome tab.

It uses the Local Storage to store across multiple refreshes as to be able to opne up the extension and save your saved leads across multple chrome tabs and windows.

#### As seen below the save current tab function which uses chrome api to get the current tab.

``` Javascript
tabBtn.addEventListener("click", function () {
  chrome.tabs.query({ active: true, currentWindow: true }, function (tabs) {
    console.log(tabs[0].url)
    myLeads.push(tabs[0].url);
    localStorage.setItem("myLeads", JSON.stringify(myLeads));
    render(myLeads);
  });
});

```

![image](Leads-Saver/README%20IMAGES/LeadTracker%20Tab%20Saver.png)
