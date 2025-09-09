# Medical Content Quality Checker (Streamlit Demo)

一个展示 **AI 辅助医学文本审核** 的小型 Demo，功能包括：
- 医学事实核查  
- 合规与风险识别（夸大疗效 / 虚假宣传 / 敏感违规内容）  
- 面向患者的可读性评分与改写建议  

> ⚠️ 免责声明：本工具仅用于演示和研究，不可替代专业医生意见或正式合规审核。

---

## 快速开始 (Quick Start)

### 1) 环境准备
克隆仓库并安装依赖：
```bash
git clone https://github.com/fjanna/medical-content-quality-checker.git
cd medical-content-quality-checker
python -m venv .venv
source .venv/bin/activate   # Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
````

### 2) （可选）启用大模型

如果希望启用 GPT 辅助审核，需要配置 OpenAI API Key。

macOS / Linux / WSL:

```bash
export OPENAI_API_KEY="**sk-替换成你自己的Key**"
export OPENAI_MODEL="gpt-4o-mini"   # 可选，默认就是 gpt-4o-mini
```

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="**sk-替换成你自己的Key**"
$env:OPENAI_MODEL="gpt-4o-mini"
```

Windows CMD:

```cmd
setx OPENAI_API_KEY "**sk-替换成你自己的Key**"
setx OPENAI_MODEL "gpt-4o-mini"
```

⚠️ 如果没有 Key，也能运行，只是只能使用规则审核部分。

---

### 3) 启动应用

```bash
streamlit run app.py
```

运行后，终端会显示本地地址（默认 [http://localhost:8501），复制到浏览器即可访问。](http://localhost:8501），复制到浏览器即可访问。)

---

## 功能说明

* 输入一段医学文本（如患者问答、健康科普、病例描述）
* 内置 **规则引擎** 检查常见风险（始终启用）
* 可选 **大模型增强**（需要 API Key），生成结构化 JSON 审核结果
* 最终输出包括：

  * ✅ 合格
  * ⚠️ 存疑
  * ❌ 不合格
* 提供修改建议 + 患者友好改写版本

---

![首页截图](**screenshots/home.png**)
![审核结果截图](**screenshots/result.png**)
```
