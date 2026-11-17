# 京津冀工业用户用氢接收点资料采集

现有项目保存工业接入公告与图纸的冻结响应。transport 核对请求与字节来源，domain 提取资料身份，ledger 原子保存原文与版本，view 呈现已接收资料及缺口。合成样例不访问真实站点；业务关联和完整性判断尚未实现。

Python 3.11 以上，在项目根目录执行：

    python -m unittest discover -s tests -v
    python -m compileall -q capture_service tests
    python -m capture_service.cli inspect data/normal.json

Docker 构建和运行：docker build -t hydrogen-collection-007 .；docker run --rm hydrogen-collection-007。
