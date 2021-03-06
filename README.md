# cfn-diagram
![Node.js CI](https://github.com/mhlabs/cfn-diagram/workflows/Node.js%20CI/badge.svg)

CLI tool to visualise CloudFormation templates as diagrams. 

## Installation
`npm i -g @mhlabs/cfn-diagram`

## Usage
```
Usage: cfn-dia [options] [command]

Options:
  -v, --vers            output the current version
  -h, --help            display help for command

Commands:
  draw.io|d [options]   Generates a draw.io diagram from a CloudFormation template
  html|h [options]      Generates a vis.js diagram from a CloudFormation template
  help [command]        display help for command
  ```

## Output formats

### Draw.io
Use it in combination with the [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio) for VS Code to instantly visualise your stacks.

![Demo](https://raw.githubusercontent.com/mhlabs/cfn-diagram/master/demo.gif)

#### Example 
```
cfn-dia draw.io -t template.yaml
```

#### Features 
* Select only the resource types you want to see. This lets you skip granlar things like roles and policies that might not add to the overview you want to see
* Navigate through a new differnet layouts
* Works for both JSON and YAML templates
* Filter on resource type and/or resource names

### HTML
The HTML output uses [vis.js](https://github.com/visjs/vis-network) to generate an interactive diagram from your template.

![Demo](https://raw.githubusercontent.com/mhlabs/cfn-diagram/master/demo-html.gif)

#### Example 
```
cfn-dia html -t template.yaml
```


## Known issues
* Some icons are missing. Working on completing the coverage.
