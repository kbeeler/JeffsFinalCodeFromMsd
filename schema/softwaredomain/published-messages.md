# The Software Domain Publishes The Following Messages


## `SoftwareItemCreated`

**Topic:** : `company.com.software.added`

```csharp
public class SoftwareItemCreated 
{
    [Required]
    public string Id { get; set; } = string.Empty;
    [Required, MinLength(5), MaxLength(200)]
    public string TitleName { get; set; } = string.Empty;
    [Required]
    public string Publisher { get; set; } = string.Empty;
    [Required]
    public string SupportTech { get; set; } = string.Empty;

}

```

## `SoftwareItemRetired`

**Topic:**: `company.com.software.retired`

```csharp
public class SoftwareItemRetired
{
  
    [Required]
    public string Id { get; set; } = string.Empty;
  
}
```

## `company.com.software.userissuereceived"`

```csharp

public record UserIssueLogged(string IssueId, DateTimeOffset When);
```

## `company.com.software.userissuerannotated`

```csharp

public class UserEventAnnotation
{
    public int Id { get; set; }
    public string Note { get; set; } = string.Empty;
}
```
