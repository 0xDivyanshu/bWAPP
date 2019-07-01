# bWAPP
Some bWAPP solutions :)

# A8 - Cross Site Request Forgery(CSRF)
Below are the POC html pages. Open them in your server and click on button to perform the attack

## Cross-Site Request Forgery (Change Password)

- Security-Level : Low

    Please refer to [csrf_1](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_1_low.html) for solution.
    
- Security-Level : Medium
    
    Please refer to [csrf_1](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_1_medium.html) for solution.
    
- Security-Level : High
    
    Please refer to [csrf_1](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_1_high.html) for solution.

## Cross-Site Request Forgery (Change Secret)

- Security-Level : Low
    
    Please refer to [csrf_2](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_2_low.html) for solution.

- Security-Level : Medium

    Please refer to [csrf_2](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_2_medium.html) for solution.
    
- Security-Level : High

    Please refer to [csrf_2](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_2_high.html) for solution.
    
## Cross-Site Request Forgery (Transfer Amount)

- Security-Level : Low

    Please refer to [csrf_3](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_3_low.html) for solution.
    
- Security-Level : Medium

    Please refer to [csrf_3](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_3_medium.html) for solution.
    
- Security-Level : High

    Please refer to [csrf_3](https://github.com/divyanshu29/bWAPP/blob/master/CSRF/csrf_3_high.html) for solution.

# A-10 Unvalidated Redirects & Forwards
Below are the request that should be made for Open Redirection .

## Unvalidated Redirects & Forwards (1)

- Security-Level : Low
    Code Snippet :
    ```
    if(isset($_REQUEST["url"]) && ($_COOKIE["security_level"] != "1" && $_COOKIE["security_level"] != "2")){
    // Debugging
    // echo $_REQUEST["url"];
    
    header("Location: " . $_REQUEST["url"]);

    exit;
    }
    ```
    
    Please refer to [open_1](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_1_low) for solution.
    
- Security-Level : Medium
    
    Please refer to [open_1](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_1_medium) for solution.
   
- Security-Level : High
    
    Please refer to [open_1](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_1_high) for solution.
    
