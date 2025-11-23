# Progress & Meter

Two other new elements are `<progress>` and `<meter>`. These are used to show progress and levels of completion. They are very similar, but `<progress>` is used to show progress, while `<meter>` is used to show levels of completion.

## Progress Bars

The `<progress>` element is used to show progress.

Attributes:

- `max` - Describes how much work the task indicated by the progress element requires. The max attribute, if present, must have a value greater than 0. The default value is 1.

- `value` - Specifies how much of the task that has been completed. It must be a number between 0 and max, or between 0 and 1 if max is omitted. If there is no value attribute, the progress bar is indeterminate; this indicates that an activity is ongoing with no indication of how long it is expected to take.

Example:

```html
<label for="file">File progress:</label>
<progress id="file" max="100" value="70">70%</progress>
```

We can also use a progress element as a loader for a particular region:

```html
<div aria-busy="true" aria-describedby="progress-bar">
  <!-- content is for this region is loading -->
</div>

<!-- ... -->

<progress id="progress-bar" aria-label="Content loading…"></progress>
```

The `aria-busy` attribute is used to indicate that the element is busy. The `aria-describedby` attribute is used to point to the progress bar that is showing the progress of the loading. You would then remove the `aria-busy` attribute when the loading is complete. This would be done via JavaScript.

## Meters

Use the `<meter>` element to display a scalar value within a given range (a gauge):

Attributes:

- `min` - The minimum value in the range of permitted values.
- `max` - The maximum value in the range of permitted values.
- `value` - The current numeric value. This must be between the min and max attributes.
- `low` - The upper numeric bound of the low end of the measured range. This must be greater than the min, and it also must be less than the high value and max. If unspecified, or if less than the minimum value, the low value is equal to the minimum value.
- `high` - The lower numeric bound of the high end of the measured range. This must be less than the max, and it also must be greater than the low value and min. If unspecified, or if greater than the maximum value, the high value is equal to the maximum value.
- `optimum` - Indicates the optimal numeric value. It must be within the range (as defined by the min attribute and max attribute). When used with the low attribute and high attribute, it gives an indication where along the range is considered preferable. For example, if it is between the min attribute and the low attribute, then the lower range is considered preferred. The browser may color the meter's bar differently depending on whether the value is less than or equal to the optimum value.

Examples:

```html
<label for="disk_c">Drive C:</label>
<meter id="disk_c" value="2" min="0" max="10">2 out of 10</meter><br />
<label for="disk_c">Drive D:</label>
<meter id="disk_c" value="6" min="0" max="10">6 out of 10</meter><br />
```

Using the `low`, `high`, and `optimum` attributes:

```html
<meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="50">
  at 50/100
</meter>
```

Here, the meter is 50% full. The low and high values are 33% and 66%, respectively. The optimum value is 80%.

I know we haven't gotten into CSS yet, but let's say you wanted the bar to be blue when in the optimal value. You could add the following CSS:

```css
 <style>
      meter::-webkit-meter-optimum-value {
        background: blue;
      }
    </style>
```
