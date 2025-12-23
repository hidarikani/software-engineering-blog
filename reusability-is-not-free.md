# Reusability Isn't Free

Back in university I was taught that reusability is one of the pillars of good software engineering. The idea is seductive, especially for junior developers: write code once, use it everywhere, and guarantee consistent behavior.

In reality, reusability is a double-edged sword. Writing less code and maximizing its value sounds like a no-brainer, but maintenance and regression testing often tell a different story.

Consider two common scenarios:

1. A product owner requests a small feature update. It looks simple—maybe two story points. But then you realize the feature is reused in five different places. Suddenly, regression testing costs multiply, especially if automated test coverage is weak.

2. You build a reusable component for a single use case. It works fine, until you test it against two more. Suddenly, the public API isn’t flexible enough. Refactoring becomes unavoidable, scope creeps, and you start questioning whether the component will still hold up when a new use case appears in a year or two.

Reusability isn’t free—it shifts complexity into future maintenance and testing. The trick is knowing when it genuinely adds value and when it’s just adding hidden costs.

> [!NOTE]
> Licensed under CC BY-NC 4.0
