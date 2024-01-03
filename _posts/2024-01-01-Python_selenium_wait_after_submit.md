
# Table of Contents

1.  [Python selenium wait after submit](#orgb4820ac)


<a id="orgb4820ac"></a>

# Python selenium wait after submit

    check until url changes

    # save current page url
      current_url = driver.current_url
    
      # initiate page transition, e.g.:
      search_form.clear()
      search_form.send_keys(name)
      search_form.submit()
    
      # wait for URL to change with 15 seconds timeout
      WebDriverWait(driver, 15).until(EC.url_changes(current_url))

