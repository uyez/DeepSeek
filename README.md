# DeepSeek linux服务器部署教程，支持 DeepSeek-R1 671b linux远程部署，deepseek 本地部署硬件配置要求
支持Linux服务器 DeepSeek 本地部署，也支持远程linux服务器部署 DeepSeek。

### 准备工作：
1、VPS服务器：[点击查看>>](https://www.vultr.com/?ref=9630595-9J)<br>
2、搭建工具：[点击下载>>](https://www.hostbuf.com/t/988.html) ，[备用下载>>](https://dl.hostbuf.com/finalshell3/finalshell_windows_x64.exe)

### DeepSeek 本地部署硬件配置要求：
<table border="1" cellpadding="10" cellspacing="0" data-draft-node="block" data-draft-type="table" data-size="normal" data-row-style="striped">
      <tbody>
        <tr>
          <th>模型版本</th>
          <th>模型大小</th>
          <th>CPU</th>
          <th>显卡</th>
          <th>显存</th>
          <th>内存</th>
        </tr>
        <tr>
          <th>1.5B</th>
          <td>1.1GB</td>
          <td>普通四核或六核处理器</td>
          <td>要求很低</td>
          <td>2-4 GB</td>
          <td>8GB RAM</td>
        </tr>
        <tr>
          <th>7B</th>
          <td>4.7GB</td>
          <td>6核或8核处理器</td>
          <td>NVIDIA 3060 或更强的显卡</td>
          <td>8-10 GB</td>
          <td>16GB RAM</td>
        </tr>
        <tr>
          <th>8B</th>
          <td>4.9GB</td>
          <td>6核或8核处理器</td>
          <td>NVIDIA 4070 或更强的显卡</td>
          <td>10-16 GB</td>
          <td>32GB RAM</td>
        </tr>
        <tr>
          <th>14B</th>
          <td>9GB</td>
          <td>8核以上处理器</td>
          <td>NVIDIA 4080 或更强的显卡</td>
          <td>16-24 GB</td>
          <td>32GB RAM</td>
        </tr>
        <tr>
          <th>32B</th>
          <td>20GB</td>
          <td>8核以上处理器</td>
          <td>NVIDIA 4090 或更强的显卡</td>
          <td>24-48 GB</td>
          <td>64GB RAM</td>
        </tr>
        <tr>
          <th>70B</th>
          <td>43GB</td>
          <td>12核以上处理器</td>
          <td>NVIDIA A100</td>
          <td>64 GB+</td>
          <td>128GB RAM</td>
        </tr>
        <tr>
          <th>671B</th>
          <td>404GB</td>
          <td>高性能、多核CPU，服务器配置</td>
          <td>NVIDIA A100*6张或更多显卡</td>
          <td>480GB+</td>
          <td>256GB+ RAM</td>
        </tr>
        <tr>
          <th colspan="6">仅供参考</th>
        </tr>
      </tbody>
    </table>
    <p>&nbsp;</p>
    <table width="800" border="1" cellpadding="10" cellspacing="0" data-draft-node="block" data-draft-type="table" data-size="normal" data-row-style="striped">
      <tbody>
        <tr>
          <th>模型版本</th>
          <th>模型大小</th>
          <th>CPU</th>
        </tr>
        <tr>
          <th>1.5B</th>
          <td>1.1GB</td>
          <td>M1/M2 芯片(8GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th>7B</th>
          <td>4.7GB</td>
          <td>M2/M3/M4 芯片(16GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th>8B</th>
          <td>4.9GB</td>
          <td>M2/M3/M4 芯片(16GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th>14B</th>
          <td>9GB</td>
          <td>M4/M4 Pro 芯片(24GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th>32B</th>
          <td>20GB</td>
          <td>M4/M4 Pro/M2 Max/M2 Ultra 芯片(64GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th>70B</th>
          <td>43GB</td>
          <td>M4 Max/M2 Ultra 芯片(96GB 统一内存或以上)</td>
        </tr>
        <tr>
          <th colspan="3">仅供参考</th>
        </tr>
      </tbody>
    </table>
