when HTTP_REQUEST {
    if {[string tolower [HTTP::uri]] starts_with "/contact-us" } {
        HTTP::redirect "https://[HTTP::host]:444[HTTP::uri]"
    }
}


