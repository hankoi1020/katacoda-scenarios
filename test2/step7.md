After all setup there seems not many information in those graphs

If you interested, you may try to do some activity in the database

Sample:

![圖片](https://user-images.githubusercontent.com/74434769/141350240-77fb010e-4f7b-4f5b-8305-8a5e9f63d8c1.png)


## Summary

This function can help us know the status inside the system. If insider / external attacks performed, this dashboard could alert admin to deal with it as soon as possible. 

There are some example:

- **Many login attempt error, the system might subject to brute force attack** (external)
- **Many data recevied from network, it might be a DDoS attack** (external)
- **Many data sent out or running many SELECT SQL querys, it should consider whether an insider attack performed to steal data** (insider)
- **Many DELETE querys, it might someone harming the data (insider)**
