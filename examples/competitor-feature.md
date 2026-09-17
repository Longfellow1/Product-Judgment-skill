# 示例：跟进竞品AI搜索功能 / Example: Following Competitor's AI Search Feature

**判决 / Verdict: VALIDATE FIRST / 先验证**

---

## 输入需求 / Input Demand

> 竞品App上线了AI搜索，用户可以用自然语言搜索内容，结果更智能。我们的搜索现在感觉很落后，产品和运营都在说我们要跟进，不然用户会流失。
> A competitor app launched AI search — users can search with natural language and get smarter results. Our search feels outdated now. Product and ops teams are saying we need to follow suit or we'll lose users.

---

## Strike 1: 病灶命名 / Disease Diagnosis

**病型 / Pattern: 竞品焦虑症（重度）/ Competitor Anxiety Syndrome (Severe)**

这个需求的触发器是"竞品上线了"，不是"我们的用户在搜索上遇到了明确的问题"。
The trigger for this demand is "competitor launched something" — not "our users have a clear, identified problem with search."

"产品和运营都在说"——这是内部情绪传导，不是用户数据。
"Product and ops teams are saying" — this is internal emotional contagion, not user data.

"用户会流失"——这是假设，不是证据。
"Users will churn" — this is an assumption, not evidence.

这是教科书级别的竞品焦虑症：被竞品的发布节奏控制了自己的产品节奏。
This is textbook competitor anxiety: letting the competitor's release cadence control your product roadmap.

---

## Strike 2: 假设审讯 / Assumption Interrogation

**需求成立，需要以下假设全部为真：**
**This demand requires ALL of the following to be true:**

| # | 假设 / Assumption | 验证状态 / Status |
|---|-----------------|-----------------|
| 1 | 用户真的在使用竞品的AI搜索（不只是尝鲜）/ Users are genuinely using the competitor's AI search (not just trying it out) | ❌ 未验证 / Unverified |
| 2 | AI搜索体验明显优于关键词搜索（对你们的场景）/ AI search is meaningfully better than keyword search in your specific context | ❌ 未验证 / Unverified |
| 3 | 搜索体验是用户留存的关键因素 / Search experience is a key factor in user retention | ❌ 未验证 / Unverified |
| 4 | 你们现有搜索有明确的用户痛点数据 / Your existing search has documented user pain point data | ❌ 未验证 / Unverified |
| 5 | 做完AI搜索能带来留存改善 / Building AI search will improve retention | ❌ 未验证 / Unverified |
| 6 | 你们的内容/数据质量支撑AI搜索效果 / Your content/data quality can support effective AI search | ❌ 未验证 / Unverified |

**已验证 / Verified:** 无 / None

**当前证据等级 / Current Evidence Level:** L0 — 所有起点来自"竞品上线了"这个事件，而不是数据 / All starting points come from the "competitor launched" event, not from data

**用户价值公式 / User Value Formula:**

| 维度 / Dimension | 内容 / Content |
|----------------|---------------|
| 旧体验 / Old Experience | 关键词搜索，需要输入精确词汇 / Keyword search requiring precise vocabulary |
| 新体验 / New Experience | 自然语言搜索，更容易表达模糊需求 / Natural language search, easier to express vague needs |
| 替换成本 / Replacement Cost | 几乎没有（同一个搜索框）/ Almost none (same search box) |
| 净用户价值 / Net User Value | 潜力高，但前提是内容质量够、AI效果够好 / High potential, but contingent on content quality and AI effectiveness |

**特别提示 / Special Note:**
AI搜索有一个隐性风险：如果内容库质量差，AI会把不相关的结果包装得更像答案（幻觉），比关键词搜索返回空结果更糟糕。这是很多团队没有提前想清楚的。
AI search has a hidden risk: if the content library quality is poor, AI will package irrelevant results to look more like answers (hallucination) — worse than keyword search returning no results. Most teams don't think through this in advance.

---

## Strike 3: 失败预演 / Failure Forecast

**第1个月 / Month 1:**
在竞品焦虑的氛围下快速立项，目标是"赶紧上线，不能落后"。进度压力大，测试周期压缩。
Fast-tracked under competitive anxiety. Goal: "ship quickly, can't fall behind." High schedule pressure, testing cycle compressed.

**第2-3个月 / Month 2-3:**
发现AI搜索在某些长尾内容召回效果不稳定，部分query返回结果和用户意图明显不符。团队在"继续优化"和"先上线再迭代"之间纠结。
AI search recall is unstable on long-tail content. Some queries return results clearly mismatched to user intent. Team debates "keep optimizing" vs "ship and iterate."

**第4个月 / Month 4:**
上线。媒体报道"XX也推出AI搜索"，内部情绪稳定。
Launch. Media reports "XX also launches AI search." Internal anxiety subsides.

**第5个月 / Month 5:**
数据分析：AI搜索使用率约30%，点击率和传统搜索相近，无显著提升。部分内容品类AI搜索效果明显差于关键词搜索（用户反馈"搜出来的东西很奇怪"）。
Data analysis: AI search usage rate ~30%, click-through rate similar to traditional search, no significant improvement. In some content categories, AI search performs noticeably worse than keyword search (user feedback: "the results are weird").

**第6个月 / Month 6:**
复盘：没有明显的留存改善，没有明显的流失阻止。工程投入3个月，产出了一个需要持续维护的系统和一个PR point。
Retrospective: no meaningful retention improvement, no meaningful churn prevention. 3 months of engineering investment produced a system requiring ongoing maintenance and one PR point.

**根因 / Root Cause:**
竞品有不代表竞品对，竞品对不代表你们的用户场景一样。在不了解竞品AI搜索真实用户数据、不了解自己用户搜索痛点的情况下跟进，是在用工程资源买一个"不落后"的心理安慰。
Competitor having it doesn't mean competitor is right. Competitor being right doesn't mean your user context is the same. Following without understanding the competitor's real usage data or your own users' search pain points means spending engineering resources to buy psychological reassurance about "not falling behind."

---

## 建议 / Recommendation

**在立项前，先花1-2周回答两个问题：**
**Before starting the project, spend 1-2 weeks answering two questions:**

**问题1 / Question 1 — 你们的搜索现在有多大的问题？/ How bad is your search actually?**

具体做 / Specifically do:
- 拿出搜索零结果率数据 / Pull up your zero-results rate data
- 对比搜索后跳出率 vs 非搜索路径跳出率 / Compare bounce rate after search vs non-search paths
- 统计用户投诉/反馈里关于搜索的占比 / Measure what percentage of complaints/feedback is about search
- 做5个用户访谈，让他们当场用搜索找真正想找的内容，观察他们 / Conduct 5 user interviews: watch them use search live to find something they actually want

判断标准 / Judgment criteria: 如果搜索问题不突出，这个需求的优先级应该大幅下降。/ If search problems aren't prominent, this demand's priority should drop significantly.

**问题2 / Question 2 — 竞品AI搜索用户真的在用吗？/ Are competitor users actually using AI search?**

具体做 / Specifically do:
- 找10-20个竞品用户，直接问：你用过AI搜索吗？你觉得比之前好多少？你现在主要怎么找内容？/ Find 10-20 competitor users. Ask directly: have you used AI search? How much better do you think it is? How do you mainly find content now?

判断标准 / Judgment criteria: 如果他们说"用过，感觉和以前差不多"或"我直接刷推荐"，这个需求的紧迫性进一步降低。/ If they say "tried it, feels about the same" or "I just scroll recommendations," urgency drops further.

**两个问题都有答案后，再决定：做、不做、还是从另一个角度解决搜索问题。**
**After both questions are answered, decide: build, don't build, or solve the search problem from a different angle.**
