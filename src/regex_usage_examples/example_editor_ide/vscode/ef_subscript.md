# Markdown中让EF后缀变下标且加粗

正则：

```bash
`EF([^`]+)`
EF<b><sub>$1</sub></b>
```

从：

```markdown
    * EF<b><sub>IMPI</sub></b> – IMS private user identity,
    * EF<b><sub>DOMAIN</sub></b> - Home Network Domain Name,
    * `EFIMPU` - IMS Public User Identity (one or more),
    * `EFAD` - Administrative Data (UE operation mode, e.g. normal or type approval),
    * `EFARR` - Access Rule Reference (access rules for files located under the ISIM ADF),
    * `EFIST` - ISIM Service Table (lists available optional services:P-CSCF address, Generic Bootstrapping Architecture (GBA), HTTP Digest, GBA-based Local Key Establishment Mechanism, support of P-CSCF discovery for IMS local break out),
    * `EFP-CSCF` - P-CSCF Address (one or more),
    * `EFGBABP` - GBA Bootstrapping parameters (contains the AKA Random challenge (RAND) and Bootstrapping Transaction Identifier (B-TID) associate with a GBA bootstrapping procedure),
    * `EFGBANL` - GBA NAF List (contains the list of NAF_ID and B-TID associated to a GBA NAF derivation procedure)
    * `EFNAFKCA` - NAF Key Centre Address (one or more).
```

变成：

```markdown
    * EF<b><sub>IMPI</sub></b> – IMS private user identity,
    * EF<b><sub>DOMAIN</sub></b> - Home Network Domain Name,
    * EF<b><sub>IMPU</sub></b> - IMS Public User Identity (one or more),
    * EF<b><sub>AD</sub></b> - Administrative Data (UE operation mode, e.g. normal or type approval),
    * EF<b><sub>ARR</sub></b> - Access Rule Reference (access rules for files located under the ISIM ADF),
    * EF<b><sub>IST</sub></b> - ISIM Service Table (lists available optional services:P-CSCF address, Generic Bootstrapping Architecture (GBA), HTTP Digest, GBA-based Local Key Establishment Mechanism, support of P-CSCF discovery for IMS local break out),
    * EF<b><sub>P-CSCF</sub></b> - P-CSCF Address (one or more),
    * EF<b><sub>GBABP</sub></b> - GBA Bootstrapping parameters (contains the AKA Random challenge (RAND) and Bootstrapping Transaction Identifier (B-TID) associate with a GBA bootstrapping procedure),
    * EF<b><sub>GBANL</sub></b> - GBA NAF List (contains the list of NAF_ID and B-TID associated to a GBA NAF derivation procedure)
    * EF<b><sub>NAFKCA</sub></b> - NAF Key Centre Address (one or more).
```

Markdown的预览效果：

【此处由于印象笔记冲突导致帖子图片丢失】
