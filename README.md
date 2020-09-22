# Laravel Nova Fields Agent


## Description
This field give the ability to hide fields from your resources table on mobile screens for a better responsive concept.

## Screenshots
![Screenshot](screenshot.gif)

## Installation
This package can be installed through Composer.
```bash
composer require outhebox/nova-fields-agent
```

## Example Usage
Note: All Fields Supported "Text Field only for example".

```php
// Important !!!
use Outhebox\NovaFieldsAgent\HasNovaFieldsAgent;

class Example extends Resource
{
    use HasNovaFieldsAgent; // Important !!!

    /**
     * Get the fields displayed by the resource.
     *
     * @param  \Illuminate\Http\Request  $requestµµ
     * @return array
     */
    public function fields(Request $request)
    {
        Text::make('ExampleField')
            ->hideFromDetailOnMobile() // Hide the field from details page on Mobile
            ->hideFromDetailOnTablet() // Hide the field from details page on Tablet
            ->HideFromIndexOnMobile() // Hide the field from index on Mobile
            ->HideFromIndexOnTablet() // Hide the field from index on Tablet
            ->sortable(),
    }
}
```


