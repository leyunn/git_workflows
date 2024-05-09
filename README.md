### 1. Automatic Issues Labeling ([auto_labeler.yml](https://github.com/leyunn/Test/blob/main/.github/workflows/auto_labeler.yml))

**Design**

This automation is designed to automatically scan the titles and bodies of issues for keywords matching the label names when an issue is created. Once identified, these keywords trigger the automatic assignment of the corresponding label to the issue. Some labels have type (e.g. package, feat) at the front, so it would be stripped out during matching.

**Rationale**

In the Remix project, there are 77 labels, which can be categorized into two types: functional and non-functional. Functional labels, such as *"CLA signed"*, *"bug:unverified"*, and *"awaiting release"*, serve specific purposes. On the other hand, non-functional labels, such as *"package:dev"* and *"feat:cookies"*, are associated with the scope of issues. It is observed that the name of the feature or package is often mentioned in the content of the issue, therefore this automation aims to accelerate the issue triage process by automatically assigning labels to newly created issues based on their content. By categorizing issues upfront, it helps prioritize and route them more effectively, ensuring that each one is directed to the appropriate team or individual for resolution. 

### 2. Proposal Forwarding Notification ([notifier.yml](https://github.com/leyunn/Test/blob/main/.github/workflows/notifier.yml))

**Design**

This automation is designed to recognize the issue numbers mentioned in the body of the newly opened issues and automatically comment on the previous proposals.

**Rationale**

This automation addresses the need for transparency and communication in the feature development process. We observed a recurring pattern of users asking about the progression of proposals, the team would have to respond with the issue number of the newly created issue. Even though it is currently not a practice to add the related issue number in the new issues, however, by adding this mechanism, it can enhance the project's ability to respond promptly to community-reported issues, improving project stability and community satisfaction.

