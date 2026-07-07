---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# What I Learned from FCAJ Community Day

### Event Information

* **Event name:** FCAJ Community Day
* **Date & time:** Saturday, 23 May 2026, 09:00 - 12:00 GMT+7
* **Location:** Bitexco Financial Tower, 2 Hai Trieu Street, Saigon Ward, Ho Chi Minh City, Vietnam
* **Role:** Attendee

### Evidence of Participation

![Evidence of participation at FCAJ Community Day](../../images/4-EventParticipated/event2.jpg)

### Speakers and Main Topics

* **Tinh Truong** - context design and how to make AI actually useful.
* **Anh Pham** - friendly AI assistant workflows with Amazon Quick.
* **Thinh Nguyen** - CloudFront from edge to origin and why it is a strong foundation.
* **Team VIB** - building UTMorpho from idea to demo during a 36-hour hackathon.
* **Duc Dao** - non-determinism in LLM settings that appear deterministic.
* **Vy Lam** - enterprise-grade multi-agent system design for startup credit scoring.

### My Overall Impression

FCAJ Community Day was not a normal lecture-style workshop for me. It felt more like a community meetup where I could listen to real engineers, students, and builders talk about how they use AI and AWS in actual projects.

Before joining the meetup, I mostly saw AI as a tool for asking questions or generating code snippets. After the event, I understood that AI is more useful when it is placed inside a clear workflow, given enough context, and combined with good system design. I also learned that cloud architecture is not only about choosing services, but also about thinking carefully about performance, cost, security, reliability, and user experience.

### What I Learned

#### 1. AI needs good context, not only good prompts

The session about context helped me understand why some AI answers are useful while others are too generic. A prompt alone is not enough. The quality of the answer depends on the context we provide: the goal, constraints, examples, previous information, and expected output.

This changed the way I use AI during the internship. When I write reports or explain my AWS project, I now try to give more background first instead of asking a short question. For example, when documenting PeriodIQ, I need to explain my role, the Rule Engine flow, input data, and expected output before asking AI to help refine the wording.

#### 2. AI can support workflows, not just conversations

The Amazon Quick session showed me that AI assistants can be used for more than chatting. They can help explore data, create workflows, share team knowledge, and generate dashboards or reports from raw information.

From this, I learned that a useful AI product should not only answer questions. It should reduce repeated work and help users complete real tasks faster. This is a good mindset for future projects because the value of AI should be measured by how much it improves a workflow, not just by how impressive the answer sounds.

#### 3. CloudFront is more than a CDN

The CloudFront session was the most directly related to my AWS project. Before this meetup, I understood CloudFront mainly as a service for delivering static websites faster. After the session, I learned that CloudFront is also an important edge layer for routing, security, performance, reliability, and cost optimization.

This helped me understand PeriodIQ better because our frontend is hosted on S3 and served through CloudFront. The user does not interact with S3 directly. CloudFront becomes the public entry point, improves delivery performance, and can work with security controls such as WAF. This made the S3 + CloudFront part of my project feel much clearer.

#### 4. Building a product requires reducing scope

The hackathon sharing session about building UTMorpho in 36 hours taught me that teams cannot build everything at once. A good team needs to identify the core problem, reduce unnecessary features, build the main flow first, and prepare a clear demo.

This lesson is very relevant to my team project, PeriodIQ. At first, a workout planning system can become very large: user profiles, personal records, templates, progress tracking, notifications, admin pages, and many rule types. The important part is to make the main flow work first: user input -> Rule Engine -> generated 4-week plan -> saved result -> displayed on the UI.

#### 5. LLM output still needs validation

The session about non-determinism in LLMs was interesting because it showed that even when settings look deterministic, the output may still change because of model behavior and inference optimizations.

The key lesson for me is that AI systems should not be trusted blindly. If AI is used in a serious workflow, the system needs validation, fallback logic, clear constraints, and human review for important decisions. This also connects to my PeriodIQ Rule Engine: even though PeriodIQ is rule-based instead of LLM-based, generated workout plans still need constraints such as volume control, conflict resolution, and deload logic to keep the result safe.

#### 6. Multi-agent systems need clear responsibility

The final session about enterprise-grade multi-agent systems helped me understand that using many agents is not automatically better. Each agent needs a clear role, and the system needs guardrails, compliance checks, and a reason why multi-agent design is useful.

I learned that architecture should solve a real problem, not just use a popular technology. Sometimes a simple single-service or single-agent approach is better if the workflow is small. Multi-agent design makes sense only when the problem is complex enough and the responsibilities can be separated clearly.

### How I Applied This to My Internship

After the meetup, I connected several lessons back to my internship work:

* I understood the S3 + CloudFront frontend path in PeriodIQ more clearly.
* I improved how I describe technical context when writing the report and workshop pages.
* I became more careful about validation, especially for generated results.
* I learned to explain a project from problem -> solution -> architecture -> demo, instead of only listing services.
* I understood that AI and cloud services are useful only when they support a real user workflow.

### Personal Reflection

The meetup gave me a broader view of both AI and AWS. It helped me move from just learning individual services to thinking about how services and tools are combined in a real product.

For me, the most valuable lesson was that good engineering is not only about using new technology. It is about understanding the problem, giving the system enough context, designing a reliable flow, and making sure the final result is useful for users.
