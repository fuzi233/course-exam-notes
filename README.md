# Course Exam Notes Skill

一个用于把课程 PPT、PDF、tutorial、case study、past paper 和 sample answer 整理成期末复习 Markdown 笔记的 Codex skill。

## 说明

这个 skill 还没有做过系统测试，也不能保证对所有课程都有效。它主要来自我自己真实整理期末复习资料时反复使用的一套工作步骤：先审计资料来源，再看 past paper 和 sample answer，最后把内容压缩成适合记忆和答题的笔记。

如果你也在用类似流程，欢迎直接修改、提 issue 或开 PR。任何关于结构、提示词、输出格式、可验证性和实际复习效果的建议都很有价值。

## 适合做什么

- 把课程 PPT/PDF/slides 整理成 exam-ready notes
- 从 past paper 和 sample answer 反推复习重点
- 生成 source coverage audit，检查哪些资料读过、哪些没读
- 为闭卷/开卷复习压缩 definitions、core points、examples 和 exam sentences
- 给英文课程内容补一点中文助记说明

## 使用方式

把本目录作为一个 Codex skill 使用。核心文件是：

- `SKILL.md`: skill 的完整工作流和输出要求
- `agents/openai.yaml`: 简单的展示配置

触发时可以这样描述任务：

```text
Use course-exam-notes to turn these course PDFs and past papers into concise exam revision notes.
```

或者中文也可以：

```text
用 course-exam-notes 帮我把这些课件和往年题整理成期末复习笔记。
```

## 默认输出

通常会生成两类 Markdown 文件：

- `COURSE_exam_core_notes.md`: 面向背诵和答题的核心复习笔记
- `COURSE_source_coverage_audit.md`: 资料覆盖、题型证据和遗漏项审计

## 设计原则

- 不只按课件顺序摘抄，而是按考试可用性整理
- past paper 和 sample answer 优先于泛泛总结
- 不凭文件名脑补内容，读不到就明确标记
- generated notes 只能做辅助参考，不能当主要证据
- 每个重点 topic 尽量包含 definition、core points、example、evidence 和 exam sentence

## 状态

Work in progress. 目前只是我个人真实工作流的整理版，还需要更多课程、更多资料类型和更多实际考试复习场景来验证。
