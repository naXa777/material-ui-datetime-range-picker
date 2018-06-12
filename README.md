
# [Material-UI Datetime Range Picker](http://www.material-ui.com/)

Material-UI Datetime Range Picker is a datetime range picker built off of [Material-UI](http://material-ui.com/) components.

Check out their [documentation site](http://www.material-ui.com/) for live examples.

## Installation

Material-UI Datetime Range Picker is available as an [npm package](https://www.npmjs.org/package/material-ui-datetime-range-picker).

```sh
npm install material-ui-datetime-range-picker
```

## Notes

This is still a work in progress so use it at your own risk. I've added some basic documentation. There are many attributes that need to be abstracted into a param and other work that needs to be done. Feel free to contribute!

## Usage

`import { DateRangePicker } from 'material-ui-datetime-range-picker';`

### Example:
```
<DateRangePicker
    autoOk={true}
    autoOpenField={true}
    onChange={onChange}
    onDismiss={onDismiss}
    showCalendarStatus={true}
    className="my-date-picker"
    firstDayOfWeek={0}
    dayButtonSize="6.25vw"
    calendarDateWidth="80vw"
    calendarTimeWidth="40vw"
    local='en-US'
    mode='portrait'
    startLabel='Beginning'
    endLabel='Ending'
/>
```

### Options:

<pre>
  <strong>autoOk:</strong>
    Description:
      Boolean - If true, this closes the calendar automatically when a date/time is selected.

    Default: false

  <strong>autoOpenField:</strong>
    Description:
      Boolean - If true, immediately jumps to the next input field. For example, if you just selected the start date, the start time field would open immediately.

    Default: false

  <strong>onChange(e, selection):</strong>
    Description:
      Function - Called when the datetimes have been selected for start and end.

    Default: null

    Example:
      The `selection` will be an object with start and end attributes that will either be a datetime value or falsey (undefined/null).
</pre>
```javascript
  {
    start: Wed Jun 13 2018 12:00:00 GMT-0600 (MDT),
    end: undefined
  }
```
  <pre>
      <strong>Note that if a date is not given it will be either undefined or null (falsey value).</strong>

  <strong>onDismiss(e, selection):</strong>
    Description:
      Function - Called when the picker has been closed/dismissed.

    Default: null

    Example:
      The `selection` will be an object with start and end attributes that will either be a datetime value or falsey (undefined/null).
</pre>
```javascript
  {
    start: null,
    end: null
  }
```
  <pre>
      <strong>Note that if a date is not given it will be either undefined or null (falsey value).</strong>

  <strong>showCalendarStatus:</strong>
    Description:
      Boolean - If true, this will show a header with the current field being selected.

    Default: false

    Example:
      If true, the user would see a header displaying "Start Date", "End Time", etc... or the custom labels provided.

  <strong>className:</strong>
    Description:
      String - If provided, it will allow the class styling to overwrite some basic styling of the root element.

    Default: null

  <strong>container:</strong>
    Description:
      String - Determines if the calendar/time picker should appear as a modal or inline when active.

    Default: 'dialog'

    Options: 'dialog' or 'inline'

  <strong>endLabel:</strong>
    Description:
      String - The text used to indicate the ending date/time selection fields.

    Default: 'End'

  <strong>firstDayOfWeek:</strong>
    Description:
      Integer - Used to change the first day of week. It varies from Saturday to Monday between different locales. The allowed range is 0 (Sunday) to 6 (Saturday). The default is `1`, Monday, as per ISO 8601.

    Default: 1

  <strong>dayButtonSize:</strong>
    Description:
      String - Allows you to adjust the size of the <strong>day button</strong>. It is a string because it allows you to use different units from px to vw.

    Default: '34px'

  <strong>calendarDateWidth:</strong>
    Description:
      String - Allows you to adjust the width of the <strong>day</strong> picker. It is a string because it allows you to use different units from px to vw.

    Default: '310px'

  <strong>calendarTimeWidth:</strong>
    Description:
      String - Allows you to adjust the width of the <strong>time</strong> picker. It is a string because it allows you to use different units from px to vw.

    Default: '125px'

  <strong>locale:</strong>
    Description:
      String - The locale for calculating the datetime.

    Default: 'en-US'

  <strong>mode:</strong>
    Description:
      String - Determines the rotation of the calendar.

    Default: 'portrait'

    Options: 'portrait' or 'landscape'

  <strong>startLabel:</strong>
    Description:
      String - The text used to indicate the beginning date/time selection fields.

    Default: 'Start'

  <strong>value:</strong>
    Description:
      Object - The default value for the date/time range picker

    Example:
</pre>
```javascript
  {
    start: Wed Jun 13 2018 12:00:00 GMT-0600 (MDT),
    end: Wed Jun 14 2018 12:00:00 GMT-0600 (MDT)
  }
  ```
  <pre>

## Contributions:

I don't have a lot of time to maintain this repo currently. If you see any bugs, feel free to open an issue and if you have time, code contributions are always welcome.

## License
This project is licensed under the terms of the
[MIT license](https://github.com/jkslyby/material-ui-datetime-range-picker/blob/master/LICENSE)
