+++
date = '2026-11-18T20:41:37-05:00'
draft = false
title = 'Your Website Doesnt Need Another Framework'
description = 'A reflection on JavaScript frameworks, unnecessary complexity, and why native web technologies are still worth learning.'
tags = ["Web Development"]
+++

There is a particular feeling that comes with discovering a new JavaScript framework.

The documentation looks promising, the examples are impressive, and suddenly you start imagining how much better your next project could be with it.

Before long, a simple website becomes an opportunity to configure a build system, install dependencies, create components, manage state, and organize a folder structure that sometimes feels more complicated than the website itself.

I've seen this pattern often enough to ask a simple question:

**Do we really need all of that?**

## The web was already capable of doing quite a lot

HTML, CSS, and JavaScript are not outdated technologies waiting to be replaced. They are the foundation of the web, and they continue to evolve.

You can create accessible navigation, responsive layouts, interactive elements, animations, and complete user experiences without necessarily introducing a framework.

Consider a simple interaction:

```html
<button id="toggle-button" aria-expanded="false">
  Show more
</button>

<p id="extra-content" hidden>
  Here is some additional information.
</p>

<script>
  const button = document.querySelector("#toggle-button");
  const content = document.querySelector("#extra-content");

  button.addEventListener("click", () => {
    const isExpanded =
      button.getAttribute("aria-expanded") === "true";

    button.setAttribute("aria-expanded", String(!isExpanded));
    content.hidden = isExpanded;
  });
</script>
```

This isn't particularly sophisticated, and that's precisely the point.

For a small interaction, native JavaScript is perfectly capable of doing the job.

You don't need a component library, a state management solution, or an entire application architecture to show and hide a paragraph.

## Complexity has a cost

Frameworks solve real problems. They help developers organize large applications, reuse components, manage complex state, and maintain consistent development patterns.

But every additional tool introduces something else to understand and maintain.

There are dependencies to update, configuration files to manage, conventions to follow, and sometimes breaking changes to deal with.

None of these things are inherently bad. They simply have a cost.

And that cost makes sense when the project benefits from the abstraction. It becomes harder to justify when the framework is doing very little beyond what the browser already provides.

<!-- IMAGE: An editorial-style photograph of a laptop displaying a clean HTML and CSS code editor, with a minimal desk setup. The composition should communicate simplicity and focus. Place it here, between this section and the next. -->

## Choose the tool after understanding the problem

I don't think the answer is to avoid frameworks altogether. That would be just another unnecessary rule.

The important thing is to understand why you're choosing a particular tool.

A complex dashboard with interactive data, authentication, and multiple application states has different requirements from a personal portfolio with a few pages and a contact section.

They shouldn't necessarily be built in the same way.

Here is a simplified way to think about it:

{{< table >}}
| Project | A reasonable starting point |
|---|---|
| Personal portfolio | HTML and CSS |
| Simple landing page | HTML, CSS, and a little JavaScript |
| Interactive dashboard | A JavaScript framework |
| Content-focused blog | Static site generator |
| Complex web application | Framework with an appropriate architecture |
{{< /table >}}

These aren't strict rules. They're starting points.

The best technology depends on the actual requirements, the people maintaining the project, and the experience you want to deliver.

## Learn the platform before the abstractions

One thing I find particularly valuable about working with native web technologies is that they help you understand what happens beneath the tools you use.

Learning how the DOM works makes JavaScript frameworks easier to understand. Knowing CSS makes component libraries less mysterious. Understanding semantic HTML helps you build better interfaces regardless of your preferred technology.

Frameworks can make development more convenient, but they shouldn't become a substitute for understanding the platform.

In fact, knowing the fundamentals gives you more freedom to choose.

You can adopt a framework because it genuinely helps, or decide not to use one because your project doesn't need it.

That is a much better position than choosing a technology simply because everyone else seems to be using it.

## A smaller stack can be a deliberate decision

There is nothing particularly impressive about having a long list of dependencies.

Sometimes a project becomes better when you remove things rather than add them.

Fewer dependencies can mean less maintenance. Less configuration can mean more time spent building. And a simpler architecture can make a project easier for someone else to understand.

Of course, simplicity doesn't mean avoiding useful tools or refusing to learn new technologies.

It means being intentional about what you introduce.

The next time you start a web project, perhaps begin with a blank HTML file.

Not because frameworks are bad, but because understanding what you actually need is a good place to start.
