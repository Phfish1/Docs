# SHOW

```
$ ufw show added
```

```
$ ufw status [numbered]
```

# START

**! REMEMBER TO ADD RULES BEFORE ENABLING !**

```
$ ufw enable
```

```
$ ufw status
```

```
$ ufw reload
```

**Removes all rules** "*Resets to default*"
```
$ ufw restart
```

# `1` Rules:

```
$ ufw {allow | deny} 22[/tcp]
```

```
$ ufw delete allow 22
```

```
$ ufw delete "num"
```

### `1.1` Default Rules:

Configures a deafult on all network traffic going inbound or outbound
```
$ ufw default allow outgoing
```

```
$ ufw default deny incoming
```


### `1.2` Advanced Rules:

```
$ ufw allow "www"
```

##### Extra [UFW](https://www.linode.com/docs/guides/configure-firewall-with-ufw/)