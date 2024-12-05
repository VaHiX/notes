# How I reset Udemy courses!
There have been several times when I paused a course halfway through and later wanted to restart from the beginning, but Udemy doesn’t offer a straightforward way to do this. 
That’s when I came across this script (thanks to JohnDinhDev).

    // Stores all unexpanded section headers, and clicks on the unexpanded section headers to expand them
    const sectionEl = document.querySelectorAll("section[data-purpose='sidebar'] div.ud-btn-link");
    sectionEl.forEach((section) => {
      const isClosed = section.parentElement.querySelector("span").getAttribute("data-checked") !== "checked"
      if (isClosed) section.click()
    });
    
    // Stores all checkboxes on the page, and clicks on any checkboxes on that currently checked
    const checkboxes = document.querySelectorAll("input[type='checkbox']");
    checkboxes.forEach((checkbox) => {
      if(checkbox.checked) {
        checkbox.click();
      }
    })
    
    location.reload();

For sure with this method, you can complete the entire course without having to follow the content in order (why?).

    // Stores all unexpanded section headers, and clicks on the unexpanded section headers to expand them
    const sectionEl = document.querySelectorAll("section[data-purpose='sidebar'] div.ud-btn-link");
    sectionEl.forEach((section) => {
      const isClosed = section.parentElement.querySelector("span").getAttribute("data-checked") !== "checked"
      if (isClosed) section.click()
    });
    
    // Stores all checkboxes on the page, and clicks on any checkboxes on that currently checked
    const checkboxes = document.querySelectorAll("input[type='checkbox']");
    checkboxes.forEach((checkbox) => {
      if(!checkbox.checked) {
        checkbox.click();
      }
    })
    
    location.reload();

However, please note that this workaround doesn't work with Udemy Business.
