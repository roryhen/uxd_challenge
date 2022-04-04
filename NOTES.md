# Rory's Implementation Notes

## HTML/CSS

- I have used BEM naming for classes, which helps decouple the markup from the CSS for better maintainability.

## HTML

- I did include alt attributes on all images, but left out text on the icons on purpose, because those images are for decorative purposes since they have accompanying text.

- I used semantic elements where I could, like article, figure, h3\*, time, and a. This helps for accessibility for example so people using screen readers can understand/traverse the document better. As a bonus it helps search bots also understand the document so a plus for SEO.

  > _\*The h3 is my best guess since we don't know the context of the heading in the document, but ideally we would be able to dynamically set a heading level (for example with a prop) on the component to optimize for accessibility._

- Since multiple sizes were provided, I used a responsive image tag, where I specified the multiple sizes that the browser can intelligently choose based on device, saving unneccessary data transfer for devices that don't need to download a larger size image.

- I also added width & height attributes on all image tags, which should be done to prevent shifting the layout when the page/app loads, Google calls this Cumulative Layout Shift, and can hurt SEO if they are not present.

## CSS

- I made the component full-width by default, since it will most likely be used in a container that defines it's own sizing, or the consumer of the component can use a utility class to define the width.

- I used 'system-ui' (uses the device's system font) as a fallback font because it has good browser support.

- For the green bar on the side, common in UI practices, I inferred it was meant to convey the status of the component. In this case being green most likely being a "success" status. So I included other possible statuses like a info status, warning status, or danger status that would be applied via a modifier class on the component.

- I added font smoothing to improve the appearance of text.

- I accommodated for varying lengths of content for the URL location and the title that would likely occur when the component is used in different contexts. If the text overflows the content is clipped and an ellipsis is shown. I specfically defined for the title to only show a maximum of two lines, after which extra text would be clipped.

- I changed the card layout for mobile screens, moving the text content below the other elements to utilize the limited amount of space available.
