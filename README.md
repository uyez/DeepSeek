# DeepSeek linux服务器部署教程，支持 DeepSeek-R1 671b linux远程部署，deepseek 本地部署硬件配置要求
支持Linux服务器 DeepSeek 本地部署，也支持远程linux服务器部署 DeepSeek。<br/>
视频教程：https://youtu.be/L5T7N9LFjro

### 准备工作：
1、VPS服务器：[点击查看>>](https://www.vultr.com/?ref=9630595-9J)<br>
2、搭建工具：[点击下载>>](https://www.hostbuf.com/t/988.html) ，[备用下载>>](https://dl.hostbuf.com/finalshell3/finalshell_windows_x64.exe)

### 一、开始部署：
1、更新VPS服务器

    apt-get update -y

2、下载 Ollama

    curl -fsSL https://ollama.com/install.sh | sh

3、下载 DeepSeek-R1模型，[点击下载>>](https://ollama.com/library/deepseek-r1)

### 二、放行端口：

    ufw allow 11434
    ufw status

### 三、设置环境变量：
1、编辑 ollama.service

    vim /etc/systemd/system/ollama.service

2、在 [Service] 部分，Environment下面添加：

    Environment="OLLAMA_HOST=0.0.0.0"
    Environment="OLLAMA_ORIGINS=*"

3、保存并退出<br/>
按【ESC】键，再输入“:wq”保存退出

4、重新加载 systemd 并重启 Ollama：

    systemctl daemon-reload
    systemctl restart ollama

<br/>

#### 查看 Ollama 运行状态：

    systemctl status ollama
    按【q】退出

#### 查看显存占用：

    nvidia-smi
    apt-get install nvtop -y
    nvtop

### 四、安装客户端使用 DeepSeek ：
安装 Chatbox AI [点击查看>>](https://chatboxai.app/zh#download)<br/>
支持在 Windows, macOS, iOS, Android, Linux 使用。

<br/>
<hr/>
<br/>

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
