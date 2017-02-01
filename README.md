# Block iOS Updates

## Function
Using the Global HTTP Proxy payload within a configuration profile, we redirect traffic heading to Apple's iOS update servers to a blank page.

## Tested Environment(s)
#### Server
* RHEL 7, CentOS 7
* Apache (httpd)

#### Client
* iOS 10.x

## Dependancies
1. Web server such as Apache or Nginx
2. MDM server such as Jamf Pro

## Configuration
1. Install Apache
    1. `sudo yum install httpd`
2. Clone repo into web root
    3. `cd /var/www/html/`
    4. `git clone https://github.com/macfanatic-ca/blockiOSUpdates.git`
3. Test pac.js availability in a browser (https://example.com/blockiOSUpdates/pac.js)
4. Create iOS Config Profile with Global HTTP Proxy payload
5. Use URL from step 3 to specify PAC file

## Changelog
**v1.0 (2017-01-28)**
* Original Release
