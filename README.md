
## Currently Not Working - suffers from an Infinite loop.

original work done by: https://github.com/sflynn1812/xslt-diff

This is an XSLT comparison script that compares the variable file b.xml with the input xml and outputs the difference using XSLT 1.0 in an exslt standard.

I have designed this as an orderless comparison with node rearrangement in the parent not being regarded as a difference.

It is a one sided comparison so differences will only be items in the input xml not in the b.xml

For instance:

input.xml

```
<root>
  <a test="test"></a>
  <b></b>
  <c></c>
</root>
```
b.xml

```
<root>
  <a test="not-this-test"></a>
  <b></b>
  <d></d>
</root>
```

Would output:

```
<comparison-result>
  <mismatch>
     <a test="test"></a>
  </mismatch>
  <mismatch>
     <c></c>
  </mismatch>
</comparison-result>
```
