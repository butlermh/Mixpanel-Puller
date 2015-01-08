Mixpanel-Puller
===============

Mixpanel-Puller is a simple python library for exporting Mixpanel data. Works by pulling data via [Mixpanel's export api](https://mixpanel.com/docs/api-documentation/data-export-api). Output is written to S3.

##Usage

Run ```./mixpanel -h``` for usage instructions. Requires that [s3cmd](http://s3tools.org/s3cmd) is installed and configured properly.

Example usage:

```
./mixpanel --apikey MIXPANEL_API_KEY --apisecret MIXPANEL_API_SECRET --startdate 2013-08-01 \
  --enddate 2013-09-01 --bucket your_s3_bucket/some_directory
```

You can find your Mixpanel keys by logging into your Mixpanel account, clicking the "Account" link on the upper right corner, and then selecting the "Projects" tab.

If they are set, it will use the following environment variables: `MIXPANEL_KEY`, `MIXPANEL_SECRET` and `S3_BUCKET`.
