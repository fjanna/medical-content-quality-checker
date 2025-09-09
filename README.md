# medical-content-quality-checker
对输入的医学文本进行 事实核查 / 合规性识别 / 易读性评分，给出「合格 / 存疑 / 不合格」结论与可操作修改建议。无 Key 时走规则引擎；有 Key 时自动调用大模型增强评估（支持 OPENAI_API_KEY）。
