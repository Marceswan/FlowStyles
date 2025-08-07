# FlowStyles - Salesforce Flow Styling Library

FlowStyles is a collection of custom labels that provide pre-configured SLDS (Salesforce Lightning Design System) styling components for use in Salesforce Flows. These labels allow you to easily apply consistent, professional styling to your Flow screens without writing custom CSS.

## 📋 Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Custom Labels Reference](#custom-labels-reference)
  - [Badges](#badges)
  - [Boxes](#boxes)
  - [Notifications](#notifications)
  - [Section Headers](#section-headers)
- [Examples](#examples)
- [Contributing](#contributing)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/Marceswan/FlowStyles.git
   ```

2. Deploy to your Salesforce org:
   ```bash
   sf project deploy start --source-dir force-app
   ```

## Usage

In your Salesforce Flow:

1. Add a **Display Text** component to your Flow screen
2. Click on the resource picker and select **Custom Label**
3. Choose the appropriate FlowStyles label (e.g., `FlowStyles_Badge_Success`)
4. Add your content after the label - Salesforce will automatically close the HTML tags

### Important Note
Salesforce automatically closes HTML tags in Flow Display Text components. Simply add your content after the custom label reference.

## Custom Labels Reference

### Badges

Small, inline status indicators perfect for highlighting key information.

| Label Name | Description | SLDS Classes | Use Case |
|------------|-------------|--------------|----------|
| `FlowStyles_Badge` | Standard badge | `slds-badge` | Default status indicators |
| `FlowStyles_Badge_Dark` | Dark/inverse badge | `slds-badge slds-badge_inverse` | High contrast badges |
| `FlowStyles_Badge_Light` | Light badge | `slds-badge slds-badge_lightest` | Subtle status indicators |
| `FlowStyles_Badge_Success` | Success badge (green) | `slds-badge slds-theme_success` | Positive status/completion |
| `FlowStyles_Badge_Warning` | Warning badge (yellow) | `slds-badge slds-theme_warning` | Caution/attention needed |
| `FlowStyles_Badge_Error` | Error badge (red) | `slds-badge slds-theme_error` | Errors/critical issues |

### Boxes

Container elements for grouping related content with various theme options.

| Label Name | Description | SLDS Classes | Use Case |
|------------|-------------|--------------|----------|
| `FlowStyles_Box` | Standard box | `slds-box slds-box_small` | Basic content container |
| `FlowStyles_Box_Shaded` | Shaded background box | `slds-box slds-box_small slds-theme_shade` | Highlighted sections |
| `FlowStyles_Box_DarkBlue` | Dark blue box | `slds-box slds-box_small slds-theme_inverse` | Important callouts |
| `FlowStyles_Box_DarkBlueAlt` | Alternative dark blue | `slds-box slds-box_small slds-theme_alt-inverse` | Secondary callouts |
| `FlowStyles_Box_Success` | Success box (green) | `slds-box slds-box_small slds-theme_success` | Success messages |
| `FlowStyles_Box_Warning` | Warning box (yellow) | `slds-box slds-box_small slds-theme_warning` | Warning messages |
| `FlowStyles_Box_Error` | Error box (red) | `slds-box slds-box_small slds-theme_error` | Error messages |
| `FlowStyles_Box_Info` | Info box (blue) | `slds-box slds-box_small slds-theme_info` | Informational content |

### Notifications

Scoped notification banners for important messages.

| Label Name | Description | SLDS Classes | Use Case |
|------------|-------------|--------------|----------|
| `FlowStyles_ScopedNotification_Light` | Light notification | `slds-scoped-notification slds-scoped-notification_light` | General notifications |
| `FlowStyles_Notification_Dark` | Dark notification | `slds-scoped-notification slds-scoped-notification_dark` | High-priority alerts |
| `FlowStyles_Notification_Success` | Success notification | `slds-scoped-notification slds-theme_success` | Success confirmations |
| `FlowStyles_Notification_Warning` | Warning notification | `slds-scoped-notification slds-theme_warning` | Warning alerts |
| `FlowStyles_Notification_Error` | Error notification | `slds-scoped-notification slds-theme_error` | Error alerts |

### Section Headers

Headers for organizing content into sections.

| Label Name | Description | SLDS Classes | Use Case |
|------------|-------------|--------------|----------|
| `FlowStyles_SectionTitle` | Section title | `slds-section slds-section__title slds-theme_shade slds-p-horizontal_small slds-p-vertical_xxx-small` | Section dividers |
| `FlowStyles_Sectionheader` | Section header | `slds-section slds-is-open slds-section__title slds-theme_shade slds-p-horizontal_small` | Collapsible sections |

## Examples

### Using a Success Badge in Flow

1. Add a Display Text component
2. Select Custom Label: `FlowStyles_Badge_Success`
3. In the rich text editor, add:
   ```
   {!$Label.FlowStyles_Badge_Success}Approved
   ```

### Creating a Warning Box

1. Add a Display Text component
2. Select Custom Label: `FlowStyles_Box_Warning`
3. In the rich text editor, add:
   ```
   {!$Label.FlowStyles_Box_Warning}
   Please review the following items before proceeding:
   • Item 1
   • Item 2
   ```

### Displaying an Error Notification

1. Add a Display Text component
2. Select Custom Label: `FlowStyles_Notification_Error`
3. In the rich text editor, add:
   ```
   {!$Label.FlowStyles_Notification_Error}
   An error occurred while processing your request. Please try again.
   ```

## Best Practices

1. **No closing tags needed**: Salesforce automatically closes HTML tags in Flow Display Text components
2. **Test in sandbox first**: Preview your flows before deploying to production
3. **Use semantic styling**: Choose labels based on meaning (success, error) not just color
4. **Combine with Flow variables**: Use merge fields to display dynamic content within styled containers
5. **Keep content simple**: Use plain text or basic formatting after the label reference

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Resources

- [Salesforce Lightning Design System](https://www.lightningdesignsystem.com/)
- [Salesforce Flow Documentation](https://help.salesforce.com/s/articleView?id=sf.flow.htm)
- [Custom Labels Documentation](https://developer.salesforce.com/docs/atlas.en-us.api_meta.meta/api_meta/meta_customlabels.htm)
