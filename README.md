# ATT&CK<sup>™</sup> Navigator
The ATT&CK Navigator is designed to provide basic navigation and annotation of [ATT&CK](https://attack.mitre.org) matrices, something that people are already doing today in tools like Excel.  We've designed it to be simple and generic - you can use the Navigator to visualize your defensive coverage, your red/blue team planning, the frequency of detected techniques or anything else you want to do.  The Navigator doesn't care - it just allows you to manipulate the cells in the matrix (color coding, adding a comment, assigning a numerical value, etc.).  We thought having a simple tool that everyone could use to visualize the matrix would help make it easy to use ATT&CK.

The principal feature of the Navigator is the ability for users to define layers - custom views of the ATT&CK knowledge base - e.g. showing just those techniques for a particular platform or highlighting techniques a specific adversary has been known to use. Layers can be created interactively within the Navigator or generated programmatically and then visualized via the Navigator.

## Usage
There is an **Install and Run** section below that explains how to get the ATT&CK Navigator up and running. You can also try the Navigator out by pointing your browser [here](https://mitre.github.io/attack-navigator). The default is the [Enterprise ATT&CK](https://attack.mitre.org) domain, but the [Mobile ATT&CK](https://attack.mitre.org/mobile) domain can be utilized [here](https://mitre.github.io/attack-navigator/mobile/). See **Enterprise and Mobile Domains** below for information on how to set up the ATT&CK Navigator on local instances to use the two different domains.

**Important Note:** Layer files uploaded when visiting our Navigator instance hosted on GitHub Pages are **NOT** being stored on the server side, as the Navigator is a client-side only application. However, we still recommend installing and running your own instance of the ATT&CK Navigator if your layer files contain any sensitive content.

Use our [GitHub Issue Tracker](https://github.com/mitre/attack-navigator/issues) to let us know of any bugs or others issues that you encounter. We also encourage pull requests if you've extended the Navigator in a cool way and want to share back to the community!

*See [CONTRIBUTING.md](https://github.com/mitre/attack-navigator/blob/master/CONTRIBUTING.md) for more information on making contributions to the ATT&CK Navigator.*

## Requirements
* [Node.js](https://nodejs.org)
* [AngularCLI](https://cli.angular.io)

## Supported Browsers
* Chrome
* Firefox
* Internet Explorer
* Safari<sup>1</sup>
* Edge
* Opera

<sup>1</sup> There is a recorded issue with using the **ATT&CK Navigator** on Safari. If the user reloads the page but cancels the action when prompted, the refresh icon in the browser window remains in the `cancel reload` state. This is believed to be an issue with Safari and not with the application.

## Install and Run
#### First time
1. Navigate to the **nav-app** directory
2. Run `npm install`

#### Serve application on local machine
1. Run `ng serve` within the **nav-app** directory
2. Navigate to `localhost:4200` in browser

#### Compile for use elsewhere
1. Run `ng build` within the **nav-app** directory
2. Copy files from `nav-app/dist/` directory

## Documentation
When viewing the app in a browser, click on the **?** icon to the right of the **ATT&CK<sup>™</sup> Navigator** title to view its documentation.

## Enterprise and Mobile Domains
By default, the ATT&CK Navigator will generate a matrix view of the tactics and techniques matrix for the [Enterprise ATT&CK](https://attack.mitre.org) technology domain knowledge base. All tactics and techniques in this domain are contained within the *act* stage, which is also pre-selected by default.

To instead generate a matrix view of the [Mobile ATT&CK](https://attack.mitre.org/mobile) technology domain knowledge base, change the `domain` value in `nav-app/src/assets/config.json` to `mitre-mobile`. **Use Device Access** and **Network-Based Effects** tactics and techniques in this domain are contained within the *act* stage, which is pre-selected by default. **Obtain Device Access** tactics and techniques are contained within the *prepare* stage, which can be manually selected.

[PRE-ATT&CK](https://attack.mitre.org/pre-attack) is included in the matrix view for either domain if the *prepare* stage is manually selected within the layer control filters.

## Layers Folder
The **layers** folder currently contains a Python script that automatically generates layer files. We will continue to add content to this repository as new scripts are implemented. Also, feel free to create pull requests if you want to add new capabilities here!

The **layers** folder's **README** contains more detailed information about how to utilize this set of scripts, and **LAYERFORMATv1.md** describes version 1 of the layer file format for the Navigator.

More information on how layers are used and developed can be found in the ATT&CK Navigator documentation that can be viewed by clicking **?** when running the app in a browser.

## Related MITRE Work
#### CTI
[Cyber Threat Intelligence repository](https://github.com/mitre/cti) of the ATT&CK catalog expressed in STIX 2.0 JSON.

#### ATT&CK
MITRE’s Adversarial Tactics, Techniques, and Common Knowledge (ATT&CK™) is a curated knowledge base and model for cyber adversary behavior, reflecting the various phases of an adversary’s lifecycle and the platforms they are known to target. ATT&CK is useful for understanding security risk against known adversary behavior, for planning security improvements, and verifying defenses work as expected.

https://attack.mitre.org

#### STIX
Structured Threat Information Expression (STIX™) is a language and serialization format used to exchange cyber threat intelligence (CTI).

STIX enables organizations to share CTI with one another in a consistent and machine readable manner, allowing security communities to better understand what computer-based attacks they are most likely to see and to anticipate and/or respond to those attacks faster and more effectively.

STIX is designed to improve many different capabilities, such as collaborative threat analysis, automated threat exchange, automated detection and response, and more.

https://oasis-open.github.io/cti-documentation/

## Notice
Copyright 2018 The MITRE Corporation

Approved for Public Release; Distribution Unlimited. Case Number 18-0128.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This project makes use of ATT&CK<sup>™</sup>

[ATT&CK Terms of Use](https://attack.mitre.org/wiki/enterprise:Terms_of_Use)
