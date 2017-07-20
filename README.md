# table2excel

> 特性

- 支持过滤 某个位置
- 支持过滤 img 标签
- 支持过滤 a 标签
- 支持过滤 input 标签
- 支持包含 行内样式。

> HTML代码

```
<html>
<head>
    <title>Demo Jquery Table2Excel</title>
</head>
<body>
<table style="width: 100%;" cellpadding=0 cellspacing=0 border="1" id="tblExport">
    <tr>
        <td colspan="5" align="center">
            <h2>成绩单</h2>
        </td>
    </tr>

    <tr>
        <td style='width:54pt' align="center">编号</td>
        <td style='width:54pt' align="center">姓名</td>
        <td style='width:54pt' align="center">语文</td>
        <td style='width:54pt' align="center">数学</td>
        <td style='width:54pt' align="center">英语</td>
    </tr>

    <tr>
        <td align="center">1</td>
        <td style="background-color: #00CC00;" align="center">Jone</td>
        <td style="background-color: #00adee;" align="center">90</td>
        <td style="background-color: #00CC00;" align="center">85</td>
        <td style="background-color: #00adee;" align="center">100</td>
    </tr>

    <tr>
        <td align="center">2</td>
        <td style="background-color: #00CC00;" align="center">Tom</td>
        <td style="background-color: #00adee;" align="center">99</td>
        <td style="background-color: #00CC00;" align="center">85</td>
        <td style="background-color: #00adee;" align="center">80</td>
    </tr>

</table>
<button id="btnExport">导出为Excel</button>
</body>
<script src="js/jquery-2.0.3.min.js"></script>
<script src="js/jquery.table2excel.js"></script>
<script type="text/javascript">
    $(document).ready(function () {
        $("#btnExport").click(function () {
            $("#tblExport").table2excel({
                exclude  : ".noExl", //过滤位置的 css 类名
                filename : "成绩单-" + new Date().getTime() + ".xls" //文件名称
            });
        });
    });
</script>
</html>


```

> 备注

- 设置 exclude 可以过滤某个位置。
- 遇到问题可以关注公众号留言。

微信名称：IT小圈儿，微信号：ToFeelings。

![IT小圈儿](https://ntaste.github.io/image/qr.jpg)

