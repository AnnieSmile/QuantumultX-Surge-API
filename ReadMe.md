## I. 关于

自制API，整理了一下

用于QuantumultX & Surge两个iOS客户端，详细来说：

- **QuantumultX**：从 ***SS订阅/SSR订阅/V2ray 订阅/Surge(conf&list)*** 转换成 **QuantumultX** 格式的订阅，并提供正则过滤，以及UDP/TFO参数的修改，以及多个订阅（托管）的合并等，以及emoji旗帜添加；
- **Surge**：从 ***Surge(conf&list)/SS订阅/V2ray订阅***，转换成 **Surge list**的格式链接，并提供正则过滤，多个订阅（托管）链接合并，以及emoji旗帜添加等



## II. 使用说明

### A. QuantumultX

| QuantumultX API     | 参数      | 说明 | 要求                                                         | 状态 |
| ------------------- | --------- | ---- | ------------------------------------------------------------ | ---- |
| 路径                | sub2quanx | NA   | https://dove.589669.xyz/sub2quanx?                           | NA   |
| 类型                | type      | 必须 | ss/ssr/v2/surge (surge的托管conf与list均可)                  | ✅    |
| 订阅链接            | sub       | 必须 | 务必先对链接urlencode，多个订阅用 + 连接                     | ✅    |
| 正则过滤节点        | filter    | 可选 | 务必先对参数urlencode                                        | ✅    |
| UDP强制更改         | udp       | 可选 | 参数为1，或0 （默认为0，关闭），对surge类型无效              | ✅    |
| TFO强制更改         | tfo       | 可选 | 参数为1，或0（默认为0，关闭），对surge类型无效               | ✅    |
| emoji 国家/地区符号 | emoji     | 可选 | 参数为 1，2（用于国行手机，无法显示台湾地区旗帜），默认为 0 关闭 | ✅    |

> 完整示范：将dler的ss订阅链接转换，并只取其中名字含 “**日本**” 的节点

```
`https://dove.589669.xyz/sub2quanx?type=ss&tfo=1&udp=1&sub=https://dler.cloud/link/xxxx?mu=ss&filter=.*%E6%97%A5%E6%9C%AC`

```



---------



### B. Surge

| Surge API           | 参数      | 说明 | 要求                                                         | 状态 |
| ------------------- | --------- | ---- | ------------------------------------------------------------ | ---- |
| 路径                | Mix2Surge | NA   | https://dove.589669.xyz/Mix2Surge?                           | NA   |
| 类型                | type      | 必须 | ss/v2/surge   （其中，surge参数对conf托管跟list通用）        | ✅    |
| 订阅(托管)链接      | sub       | 必须 | 务必先对链接urlencode，多个订阅用 + 号连接                   | ✅    |
| 正则过滤节点        | filter    | 可选 | 务必先对参数urlencode                                        | ✅    |
| v2订阅的header host | hd        | 可选 | hd=1，0 （为解决某些v2ray订阅在surge中不可用的情况，为0时，忽略header参数） | ✅    |
| UDP/TFO参数         | udp/tfo   | 可选 | 仅对type为ss的类型有效（tfo=1/0，udp=1/0 来开启/关闭，默认关闭） | ✅    |
| emoji 国家/地区符号 | emoji     | 可选 | 参数为 1，2（用于国行手机，无法显示台湾地区旗帜），默认为 0 关闭 | ✅    |

> 完整示范： 将某两个V2订阅合并转换成surge的list，并只选择其中的 **CHT ** 节点路线

```
https://dove.589669.xyz/Mix2Surge?type=v2&sub=https%3A%2F%2Fdler.cloud%2Fsubscribe%2Fxxx%3Fmu%3Dav2%2Bhttps%3A%2F%2Fytoo.xyz%2Fmodules%2Fservers%2FV2raySocks%2Fosubscribe.php%3Fsid%3D372%26token%3Dxxxo&filter=.%2ACHT
```



---

---

### 0⃣️ 请咖啡☕️名单

🙏感谢🙏

- 鸡儿硬梆梆
- 🐔哥｜法外 伉俪
- 贝贝熊🐻
- 守夜人
- Big Cat
- Xin

**如果觉得有用，请大胆请喝咖啡☕️**

<img src="https://tva1.sinaimg.cn/large/006y8mN6gy1g7t6di3i9oj30gg0g240w.jpg" style="height:300px" />



