## Echarts 代码 / 效果

[echarts](https://www.echartsjs.com/examples/zh/editor.html?c=gauge ':include :type=iframe width=100% height=800px')

## pyecharts 代码 / 效果

```python
import pyecharts.options as opts
from pyecharts.charts import Gauge

(
    Gauge(init_opts=opts.InitOpts(width="1600px", height="800px"))
    .add(series_name="业务指标", data_pair=[["完成率", 55.5]])
    .set_global_opts(
        legend_opts=opts.LegendOpts(is_show=False),
        tooltip_opts=opts.TooltipOpts(is_show=True, formatter="{a} <br/>{b} : {c}%"),
    )
    .render("gauge.html")
)
```

<iframe width="100%" height="800px" src="Gauge/gauge.html"></iframe>