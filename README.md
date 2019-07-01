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

    Code Snippet:
    ```
        switch($_REQUEST["url"])
        {
        case "1" :
            header("Location: http://itsecgames.blogspot.com");
            break;
        case "2" :
            header("Location: http://www.linkedin.com/in/malikmesellem");
            break;
        case "3" :
            header("Location: http://twitter.com/MME_IT");
            break;
        case "4" :
            header("Location: http://www.mmeit.be/en");
            break;
        default :
            header("Location: login.php");
            break;
        }
    ```
    Please refer to [open_1](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_1_medium) for solution.
   
- Security-Level : High

    Code Snippet:
    ```
        if($_COOKIE["security_level"] == "2")
    {
        // Destroys the session 
        $_SESSION = array();
        session_destroy();
        // Deletes the cookies
        setcookie("admin", "", time()-3600, "/", "", false, false);
        setcookie("movie_genre", "", time()-3600, "/", "", false, false);
        setcookie("secret", "", time()-3600, "/", "", false, false);
        setcookie("top_security", "", time()-3600, "/", "", false, false);
        setcookie("top_security_nossl", "", time()-3600, "/", "", false, false);
        setcookie("top_security_ssl", "", time()-3600, "/", "", false, false);
    }
    switch($_REQUEST["url"])
    {
        case "1" :
            header("Location: http://itsecgames.blogspot.com");
            break;
        case "2" :
            header("Location: http://www.linkedin.com/in/malikmesellem");
            break;
        case "3" :
            header("Location: http://twitter.com/MME_IT");
            break;
        case "4" :
            header("Location: http://www.mmeit.be/en");
            break;
        default :
            header("Location: login.php");
            break;
    }
    ```
    
    Please refer to [open_1](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_1_high) for solution.
    
## Unvalidated Redirects & Forwards (2)

- Security Level : Low

    Code Snippet:
    ```if(isset($_REQUEST["ReturnUrl"]) && ($_COOKIE["security_level"] != "1" && $_COOKIE["security_level"] != "2"))
    {
    // Debugging
    // echo $_REQUEST["url"];
    header("Location: " . $_REQUEST["ReturnUrl"]);
    exit;
    }
    ```
    
    Please refer to [open_2](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_2_low) for solution

- Security Level : Medium/High

    Code Snippet:
    ```
    if(isset($_REQUEST["ReturnUrl"]) && ($_COOKIE["security_level"] == "1" || $_COOKIE["security_level"] == "2"))
    {
    header("Location: portal.php");
    exit;
    }
    ```
    
    Please refer to [open_2](https://github.com/divyanshu29/bWAPP/blob/master/Open_Redirects/open_redirect_2_medium) for solution.
    
