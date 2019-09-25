## Employee Wage

The hourly wage rate that an employee will earn on a `Shift` for doing the job
specified by the `title` property of this object.

### Structure

`EmployeeWage`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | UUID for this object. |
| `employee_id` | `String` |  | The `Employee` that this wage is assigned to. |
| `title` | `String` | Optional | The job title that this wage relates to. |
| `hourly_rate` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |

### Example (as JSON)

```json
{
  "id": null,
  "employee_id": "employee_id0",
  "title": null,
  "hourly_rate": null
}
```

