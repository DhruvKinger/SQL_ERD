# Entity Relationship Diagram (ERD)

## Tables

### Artist

| Column Name | Description            |
|-------------|------------------------|
| ArtistId    | Unique identifier for each artist |
| Name        | Name of the artist     |

### Album

| Column Name | Description            |
|-------------|------------------------|
| AlbumId     | Unique identifier for each album |
| Title       | Title of the album     |
| ArtistId    | Foreign key referencing the artist |

### Track

| Column Name | Description            |
|-------------|------------------------|
| TrackId     | Unique identifier for each track |
| Name        | Name of the track      |
| AlbumId     | Foreign key referencing the album |
| MediaTypeId | Foreign key referencing the media type |
| GenreId     | Foreign key referencing the genre |
| Composer    | Name of the composer   |
| Milliseconds| Duration of the track in milliseconds |
| Bytes       | Size of the track in bytes |
| UnitPrice   | Price of the track     |

### MediaType

| Column Name | Description            |
|-------------|------------------------|
| MediaTypeId | Unique identifier for each media type |
| Name        | Name of the media type |

### PlayList

| Column Name | Description            |
|-------------|------------------------|
| PlayListId  | Unique identifier for each playlist |
| Name        | Name of the playlist   |

### PlayListTrack

| Column Name | Description            |
|-------------|------------------------|
| PlayListId  | Foreign key referencing the playlist |
| TrackId     | Foreign key referencing the track |

### Genre

| Column Name | Description            |
|-------------|------------------------|
| GenreId     | Unique identifier for each genre |
| Name        | Name of the genre       |

### Employee

| Column Name | Description            |
|-------------|------------------------|
| EmployeeId  | Unique identifier for each employee |
| LastName    | Last name of the employee |
| FirstName   | First name of the employee |
| Title       | Title of the employee  |
| ReportsTo   | EmployeeId of the employee's supervisor |
| BirthDate   | Birth date of the employee |
| HireDate    | Hire date of the employee |
| Address     | Address of the employee |
| City        | City of the employee    |
| State       | State of the employee   |
| Country     | Country of the employee |
| PostalCode  | Postal code of the employee |
| Phone       | Phone number of the employee |
| Fax         | Fax number of the employee |
| Email       | Email address of the employee |

### Customer

| Column Name | Description            |
|-------------|------------------------|
| CustomerId  | Unique identifier for each customer |
| FirstName   | First name of the customer |
| LastName    | Last name of the customer |
| Company     | Company name of the customer |
| Address     | Address of the customer |
| City        | City of the customer    |
| State       | State of the customer   |
| Country     | Country of the customer |
| PostalCode  | Postal code of the customer |
| Phone       | Phone number of the customer |
| Fax         | Fax number of the customer |
| Email       | Email address of the customer |
| SupportRepId| EmployeeId of the customer's support representative |

### InvoiceLine

| Column Name | Description            |
|-------------|------------------------|
| InvoiceLineId | Unique identifier for each invoice line |
| InvoiceId   | Foreign key referencing the invoice |
| TrackId     | Foreign key referencing the track |
| UnitPrice   | Price per unit of the track |
| Quantity    | Quantity of tracks purchased in the invoice line |

### Invoice

| Column Name | Description            |
|-------------|------------------------|
| InvoiceId   | Unique identifier for each invoice |
| CustomerId  | Foreign key referencing the customer |
| InvoiceDate | Date of the invoice     |
| BillingAddress | Billing address of the invoice |
| BillingCity | Billing city of the invoice |
| BillingState | Billing state of the invoice |
| BillingCountry | Billing country of the invoice |
| BillingPostalCode | Billing postal code of the invoice |
| Total       | Total amount of the invoice |
