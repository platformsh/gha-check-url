# Platform.sh Check a URL for a specific header response

Given a URL, performs a curl GET request and validates the server response against what we're expecting.  

## Inputs
* `test_url` - **REQUIRED**. The URL we want to test for a response. Must be a URL, not just a domain.
* `http_response` - _Optional_. The HTTP response status code we expect from the server. _Defaults to 200_
* `allow_insecure` - _Optional_. Should we use the `--insecure` flag with curl when testing the URL? _Defaults to false_

## Outputs
* None currently. 

## Example Usage
```yaml
    - name: 'Is our URL responding to requests?'
      id: test-url-for-response
      uses: platformsh/gha-check-url@main
      with:
        test_url: 'https://platform.sh/'

```

