# react-date-range
A React component for choosing dates and date ranges. Uses [Moment.js](http://momentjs.com/) for date operations.

**Live Demo :** [http://adphorus.github.io/react-date-range](http://adphorus.github.io/react-date-range)

![](https://cdn.pbrd.co/images/1fjQlZzy.png)

## Getting Started
### Installation

```
$ npm install --save react-date-range
```

## Usage
### Date Picker
```javascript
import React, { Component } from 'react';
import { Calendar } from 'react-date-range';

class MyComponent extends Component {
	handleSelect(date){
		console.log(date); // Momentjs object
	}

	render(){
		return (
			<div>
				<Calendar
					onInit={this.handleSelect}
					onChange={this.handleSelect}
				/>
			</div>
		)
	}
}

```

###### Available Options (props)
* **date:** *(String, Moment.js object, Function)* - default: today
* **format:** *(String)* - default: DD/MM/YYY
* **theme:** *(Object)* see [Demo's source](https://github.com/Adphorus/react-date-range/blob/master/demo/src/components/Main.js#L130)
* **onInit:** *(Function)* default: none
* **onChange:** *(Function)* default: none

### Range Picker
```javascript
import React, { Component } from 'react';
import { DateRange } from 'react-date-range';

class MyComponent extends Component {
	handleSelect(range){
		console.log(range);
		// An object with two keys,
		// 'startDate' and 'endDate' which are Momentjs objects.
	}

	render(){
		return (
			<div>
				<DateRange
					onInit={this.handleSelect}
					onChange={this.handleSelect}
				/>
			</div>
		)
	}
}

```

###### Available Options (props)
* **date:** *(String, Moment.js object, Function)* - default: today
* **format:** *(String)* - default: DD/MM/YYY
* **theme:** *(Object)* see [Demo's source](https://github.com/Adphorus/react-date-range/blob/master/demo/src/components/Main.js#L130)
* **onInit:** *(Function)* default: none
* **onChange:** *(Function)* default: none
* **linkedCalendars:** *(Boolean)* default: false
* **calendars:** *(Number)* default: 2
* **ranges:** *(Object)* default: none
