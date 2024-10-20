---
id: mock-date
title: Mock Date
---

When you test your stories, it might be useful to mock `new Date()` so the displayed components always render same values. You can use `meta.mockDate` parameter to set a specific date and time:

```js title="date-picker.stories.tsx"

import type { Story } from "@ginger-society/ginger-book";

export const DatePicker: Story = () => {
  const date = new Date();
  return (
    <h1>{date.toLocaleDateString("en-US")}</h1>
  );
};

DatePicker.meta = {
  mockDate: "1995-12-17T03:24:00",
};

```
