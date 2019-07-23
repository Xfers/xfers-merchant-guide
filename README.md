# xfers-merchant-guide
1 stop portal for merchant integration

Edit the /docs folder. its the source for github pages https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages 

# Templating engine
this merchant guide is powered by https://docsify.js.org/#/ 

# custom domain summary
1. go to dns provider eg: cloudflare/aws/godaddy
2. create CNAME name: merchantguide value: xfers.github.io like so:  https://cl.ly/776375a71719 
3. go to settings under github > configure it like so https://cl.ly/40b436f4af0f 
4. in step 3, github will automatically create a CNAME file in the /docs filder to inform github the url to listen to 
