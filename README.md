[![Build](https://img.shields.io/badge/build-passing-4EC820.svg?style=flat-square)](https://github.com/edward-joseph/alertBox)
[![License](https://img.shields.io/badge/license-MIT-4D9282.svg?style=flat-square)](https://github.com/edward-joseph/alertBox/blob/master/LICENSE.md)
[![Latest Stable Version](https://img.shields.io/badge/stable-v1.5.0-35A4DA.svg?style=flat-square)](https://github.com/edward-joseph/alertBox)


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/edward-joseph/alertBox">
    <img src="https://img.techpowerup.org/190623/favicon.png" alt="Logo" width="100" height="100">
  </a>

  <h3 align="center">alertBox</h3>
  <p align="center">
    Create an AlertBox with no hassle!
    <br />
    <a href="https://github.com/edward-joseph/alertBox"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/edward-joseph/alertBox/issues">Report Bug</a>
    ·
    <a href="https://github.com/edward-joseph/alertBox/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [License](#license)
* [Contact](#contact)


<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://github.com/edward-joseph/alertBox)

In fact, I needed a javascript library where I always wanted to create `alerts` and `popups` without losing any time. It's also really annoying to spend my time making different `popups` and `alerts` with different designs.

So I spent my time up:
* built a library just with javascript so libraries like jQuery no longer needed
* To make a warning message for myself and the users who are tired of writing long codes
* With just a few lines of code writing, you can create alerts and popups that even change their designs

Of course, your needs can not be addressed with this library alone, and maybe you need more than that, so I'm going to update this library to be able to meet the maximum needs.

In fact, I created this library alone, but I also asked some questions about the problem.

### Built With
This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.
* [Javascript](https://www.javascript.com)
* [Css3](http://www.css3.info)



<!-- GETTING STARTED -->
## Getting Started

To launch and use the alertBox in your project, follow the steps below.

### Prerequisites

You must first download the alertBox library from its GitHub and add it to your project.

### Installation

1. First, go to the [alertBox](https://github.com/edward-joseph/alertBox) page
2. Then download that package and add it to your project
3. To add the necessary CSS, you must first go to the [Css Folder](https://github.com/edward-joseph/alertBox/tree/master/) in the package and add the alertBox.min.css file to your css files.
4. Also, to add JS files, you must log in to the [Js Folder](https://github.com/edward-joseph/alertBox/tree/master/) and add the alertBox.js file to your js files.

<!-- USAGE EXAMPLES -->
## Usage

To work with this library, we already defined a constant variable and set it equal to the `alertBox`.

* Alert
1. To create an alert, you must first call the addAlert function. This function receives two parameters
2. The first parameter of this function is a string that contains the text inside the alert
3. The second parameter of this function is a multiplicity of objects (although giving these values is arbitrary because the defaults are predefined)


| Object Value     | Application   | Acceptable values |
| -------------    | ------------- | ----------------- |
| position         | set alert box position  | 'left', `'right'`, 'center' |
| status           | determine the status of the alert box  | `'simple'`, 'success', 'error'      |
| align            | set the text orientation of the alert box  | `'left'`, 'right', 'center'      |
| animateDelay     | latency in the alert box view  | NUMBER (s) : `0`     |
| animateDuration  | When it will take time for the alert box to be in position  | NUMBER (s) : `1`      |
| boxDuration      | The amount of time the alert box is in position  | NUMBER (s) : `2`     |

```javascript
alertBox.addAlert('This is a message',{
  position:'left',
  status:'error',
  align:'center',
  animateDelay:0.1,
  animateDuration:1,
  boxDuration:3
});
```

* Popup
1. To create a popup, you must use the `addPopup` function
2. This function receives two parameters. The first parameter of this function is an object that receives a series of values, and the second parameter of this function is a function called callback
3. The second parameter of this function receives a default value in the array, which is the first key of this array, the name of the button and the second key of the array, the number of the button that is clicked on it.

| Object Value     | Application   | Acceptable values |
| -------------    | ------------- | ----------------- |
| title         | setting the subject              | STRING: `'Subject: title'`                  |
| message         | set text message              | STRING : `'message'`                  |
| duration         | the amount of animation time              | NUMBER (s) : `1`                |
| delay         | latency in the popup view              | NUMBER (s) : `0`                |
| headerAlign         | setting the subject orientation              | `'left'`, 'right', 'center' |
| textAlign         | setting the message orientation              | `'left'`, 'right', 'center' |
| buttonAlign         | setting the buttons orientation              | `'left'`, 'right', 'center' |
| buttonWidth         | setting the buttons width              | NUMBER : `85`                 |
| buttons         | The buttons you want to display in the popup              | Object : {buttonName:`'status'`} |
| visible         | black background display              | `true`, false                  |
| hideClose         | display the exit icon              | true, `false`                  |

```javascript
alertBox.addPopup({
  duration:2,
  title:'SUBJECT',
  message:'MESSAGE',
  headerAlign:'center',
  textAlign:'left',
  buttonAlign:'right',
  buttonWidth:90,
  button:{
    Confirm:'success',
    Cancel:'error'
  },
  visible:false,
  hideClose:true
},(result) => {
  alert(result[0]+' : '+result[1]);
});
```

## License

Distributed under the MIT License. See `LICENSE` for more information.


## Contact

Edward Joseph (ALi Yaghoby) - [Edward_Joseph](https://t.me/Edward_Joseph) - alibigham3095@gmail.com

Project Link: [alertBox](https://github.com/edward-joseph/alertBox)


<!-- MARKDOWN LINKS & IMAGES -->
[build-shield]: https://img.shields.io/badge/build-passing-brightgreen.svg?style=flat-square
[license-shield]: https://img.shields.io/apm/l/MIT.svg?style=for-the-badge
[license-url]: https://github.com/edward-joseph/alertBox/blob/master/LICENSE.md
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: https://img.techpowerup.org/190623/screenshot.png
