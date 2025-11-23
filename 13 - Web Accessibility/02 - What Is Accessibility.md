# What Is Accessibility?

Let's talk about what web accessibility is. Web accessibility refers to designing and creating websites and applications in a way so that people with disabilities can use them. This includes people with visual, auditory, physical, speech, cognitive, and neurological disabilities. A big part of accessibility is making sure that your website is usable with a screen reader, which is a device for people that have impaired or loss of vision. Just like websites should be usable on all types of screen sizes, they should be usable for people with disabilities.

The W3C Web Accessibility Initiative or WAI is an effort to improve the accessibility of the World Wide Web for people with disabilities. They provide guidelines, technical specifications, and resources to help make web content, tools, and technologies accessible to people with disabilities

## Why is Accessibility Important?

1. **Inclusivity**: Accessibility ensures that all users, including those with disabilities, can access and use your website. 

2. **Legal Compliance**: Many countries have laws and regulations that require websites to be accessible, especially for government and publicly funded organizations. 

**Improved User Experience**: Accessible websites tend to offer a better user experience for everyone. Features that aid accessibility, such as clear navigation, well-structured content, and readable text, also enhance usability for people without disabilities.

**SEO Benefits**: Many accessibility practices, such as using proper HTML tags, alt text for images, and clear headings, also improve search engine optimization (SEO). Search engines can better understand and index your content, potentially leading to higher search rankings.

**Wider Audience Reach**: By making your website accessible, you reach a broader audience. People with disabilities represent a significant portion of the population, and providing them with an accessible website can increase your site's traffic and user engagement.

**Ethical Responsibility**: Providing accessible websites is an ethical responsibility. It reflects positively on your organization.

**Enhanced Brand Reputation**: Organizations that prioritize accessibility often enjoy a positive reputation and increased customer loyalty.

**Future-Proofing**: As technology evolves, new accessibility standards and best practices continue to emerge. By making your website accessible now, you are better prepared for future updates and technologies, ensuring your site remains usable and compliant over time.

## Types of Disabilities

- **Visual**: You want to create clear layouts with good contrast for the vision impaired and for blind users, your website should be adjusted for screen readers.
- **Audible**: They rely on visual content so if you have audible content, it should also be available in visual form.
- **Physical**: They rely on keyboards and other tools that use keyboard functionality. So having good keyboard interactivity is essential for these users.
- **Speech**: Alternatives for anything speech related
- **Cognitive & Nerological**: Website should be clear, logical and easy to use and navigate.

## Types Of Devices

- **Keyboard**: Many users with physical disabilities rely on keyboards instead of a mouse. Ensuring all functionality is accessible via keyboard is crucial.
- **Screen Readers**: These are software applications that read out the content of a screen for blind or visually impaired users, translating text and elements into speech or Braille.
- **Screen Magnification**: Software that enlarges text and graphics on the screen to make them more visible to users with low vision.
- **Head Pointers**: Devices that allow users to control the cursor on the screen using head movements, typically used by individuals who cannot use a mouse or keyboard.
- **Single Switch Devices**: These devices allow users to control a computer using a single button or switch, often used by individuals with severe physical disabilities.
- **Large Print Keyboards**: Keyboards with larger, high-contrast letters that are easier to see, designed for users with low vision.
- **Speech Input Software**: Software that allows users to control their computer and input text using voice commands, aiding users with physical disabilities or repetitive strain injuries.
- **Motion/Eye Tracking**: Technologies that enable users to control their devices through eye movements or other body motions, often used by individuals with severe physical disabilities.

## How to Make Your Website Accessible

There are a number of ways to make your website more accessible and we've been using a lot of them. Here are a few tips:

- Use semantic elements like `<header>`, `<nav>`, `<main>`, `<footer>`, `<article>`, `<section>`, `<aside>`, and `<figure>`. We've already learned and talked about this but this is one of the most important things that you can do to make your website accessible.
- Use alt text for images. The `alt` attribute provides a text alternative for images. This is important for people who are visually impaired and use screen readers to navigate the web.
- Use descriptive link text. Link text should be descriptive and provide context about where the link will take the user. Avoid using generic link text like "click here" or "read more."
- Use a logical tab order. The tab order is the order in which the user navigates through the page. It's important to make sure that the tab order is logical. You can do this with the `tabindex` attribute.
- Use a logical heading structure. The heading structure is the order in which the headings appear on the page. It's important to make sure that the heading structure is logical. This helps screen readers and other assistive technologies understand the structure of the content.
- Use proper labeling for inputs and other elements.
- Use ARIA attributes. ARIA attributes are used to add additional information to HTML elements. This is useful for people who use screen readers and other assistive technologies.

## More on ARIA

ARIA stands for Accessible Rich Internet Applications. It's a set of attributes that can be used to add additional information to HTML elements. It's important to use ARIA attributes because they help people who use screen readers and other assistive technologies. In many cases you don't need to use these if you're using semantic elements, adding alt text, and descriptive link text. That should be your first priority when it comes to accessibility. Keep everything semantic. But if you're using a lot of divs and spans, you may want to use ARIA attributes.

There is a saying of no ARIA is better than bad ARIA. You can make things more confusing by overusing or misusing these attributes. Keep that in mind.

These attributes begin with `aria-`. For example, `aria-label` is used to add a label to an element.

Here are some other common ARIA attributes:

- `aria-label` - Used to add a label to an element.
- `aria-labelledby` - Used to identify the element that labels the element it's applied to.
- `aria-describedby` - Used to identify the element that describes the element it's applied to.
- `aria-hidden` - Used to hide the current element from screen readers.
- `aria-expanded` - Used to indicate whether a collapsible element is expanded or collapsed.
- `aria-current` - Used to indicate the current page.
- `aria-controls` - Used to identify the element that controls the current element.
- `aria-live` - Used to indicate that an element is dynamic and will be updated.
- `aria-atomic` - Used to indicate that an element will be updated in whole, rather than in part.
- `aria-autocomplete` - Used to indicate whether a text input can be automatically completed by the browser.
