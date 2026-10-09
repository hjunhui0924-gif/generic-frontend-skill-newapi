# Interaction state matrix

For each asynchronous or editable surface, check the applicable states:

| Area | States to cover |
| --- | --- |
| Initial load | skeleton or meaningful progress, stable layout |
| Data | populated, empty, filtered-empty, partial or stale |
| Request | pending, success, recoverable error, retry |
| Form | untouched, focused, invalid, valid, submitting, submitted |
| Controls | hover, focus-visible, active, disabled, permission denied |
| Destructive action | preview or confirmation, pending, cancelled, failed |
| Feedback | inline result, toast, announcement, next action |

Prefer inline messages for field-specific problems and a toast or banner for a
completed cross-page operation. Ensure feedback is announced to assistive
technology when it is not adjacent to the triggering control.
