# Google Dynamic DNS Scripts

---

With the introduction of support for [Dynamic DNS](https://support.google.com/domains/answer/6147083?hl=en) records on Google Domains I have created two bash scripts to keep these records up to date.

* dynamicDNS - set IP to current global IP
* localDynamicDNS - set IP to current local IP

### Configuration

Update the `username` and `password` fields of the script with the username and password given to you for the dynamic DNS record, and update the `address` field with the address of the dynamic DNS record.

For example with the following Dynamic DNS:

![picutre](https://i.imgur.com/ONC1GfE.png)

The script should be configured like:

```bash
#!/bin/bash

username="FakeUsername"
password="FakePassword"
address="test.test.com"
```

### Automation

Due to DNS caching it is not recommended to run the script more frequently than once an hour using a cronjob.

