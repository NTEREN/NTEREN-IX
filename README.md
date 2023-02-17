# NTEREN-IX

位于中国大陆的一个实验性IXP

## 介绍

一个位于中国大陆的实验性IXP，主要作为非商用、中立的BGP实验交流平台，相对于已有的海外虚拟IX能让中国大陆用户获得更低的互联延迟。

本IX支持公网和DN42两个网络，具有IPv4/IPv6双栈支持。

## 接入

本IX物理位置位于：中华人民共和国陕西省西安市碑林区西安交通大学。可选接入方式：物理线路连接，或使用IX虚拟机（IXVM）进行互联。

RS公网会话限定路由来源AS。如果您愿意在IX通过RS提供Transit请提前说明。

接入请联系NaiveTomcat：Telegram [@NaiveTomcat](https://t.me/NaiveTomcat) 或发送邮件至 [tomdang@naivetomcat.cn](mailto:tomdang@naivetomcat.cn)

## 路由服务器

```
aut-num: 4242423319
as-set: AS-NTEREN:AS-NTEREN-IX
address: fe80::3319:1
```

## 参与者

| 网络 |      参与者     |    ASN     |   加入时间  |      IP      |
|------|----------------|------------|------------|--------------|
| DN42 | NAIVETOMCAT-AS | 4242423309 | 2023/02/17 | fe80::3309:1 |

## BGP社区属性

| 功能 | Extended Community | Large Community |
|-----|--------------------|------------------|
|强制向指定Peer AS宣称|(rt, 1, peeras)| (4242423319, 1, peeras)|
|不向任何Peer宣称|(rt, 0, 4242423319)|(4242423319, 0, 4242423319)|
|不向指定Peer宣称|(rt, 0, peeras)|(4242423319, 0, peeras)|
|Prepend 1x to peer|(rt, 65501, peeras)|(4242423319, 65501, peeras)|
|Prepend 2x to peer|(rt, 65502, peeras)|(4242423319, 65502, peeras)|
|Prepend 3x to peer|(rt, 65503, peeras)|(4242423319, 65503, peeras)|
|Prepend 1x to all|(rt, 65501, 4242423319)|(4242423319, 65501, 4242423319)|
|Prepend 2x to all|(rt, 65502, 4242423319)|(4242423319, 65502, 4242423319)|
|Prepend 3x to all|(rt, 65503, 4242423319)|(4242423319, 65503, 4242423319)|
