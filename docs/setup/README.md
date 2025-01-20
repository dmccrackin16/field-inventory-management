# Setup Guide

## Prerequisites

- Microsoft 365 Business Account
- SharePoint Online access
- Power Automate license
- Mobile devices for field team

## Step-by-Step Setup

### 1. Microsoft Forms Setup

1. Access Microsoft Forms:
   - Go to forms.office.com
   - Sign in with your Microsoft 365 account

2. Create New Form:
   - Click 'New Form'
   - Use template from `samples/forms/inventory-form.json`
   - Customize fields as needed

3. Form Settings:
   - Enable file uploads
   - Set response options
   - Configure sharing settings

### 2. SharePoint Configuration

1. Create Document Library:
   ```
   - Name: InventoryManagement
   - Enable versioning
   - Set appropriate permissions
   ```

2. Excel Files Setup:
   - Create inventory tracking workbook with sheets:
     - Transactions (for form responses)
     - Current Inventory (running totals)
     - Job Summary (pivot tables)
   - Enable auto-refresh
   - Set up data connections

### 3. Power Automate Flow

1. Create New Flow:
   - Trigger: When a form response is submitted
   - Actions:
     - Get form response details
     - Update Excel transactions
     - Calculate inventory totals
     - Send notifications if needed
     - Store photos in SharePoint

2. Testing:
   - Submit test form entries
   - Verify Excel updates
   - Check photo storage
   - Confirm notifications

### 4. Mobile Access

1. Form Access:
   - Create QR code for form
   - Add to Teams channels
   - Create SharePoint quick links

2. View Access:
   - Set up mobile view for inventory
   - Configure Teams dashboard
   - Test on different devices

## Troubleshooting

### Common Issues

1. Form Access:
   - Clear browser cache
   - Check permissions
   - Verify account status

2. Power Automate:
   - Check connection credentials
   - Verify file paths
   - Review error logs

3. Excel Updates:
   - Check file permissions
   - Verify formulas
   - Test data refresh

## Support

For technical support:
1. First check documentation
2. Contact system administrator
3. Submit issue on GitHub