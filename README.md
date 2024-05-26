# Jira Environment Switcher Bookmarklet
Bookmarklet to switch between Jira environments

## Getting Started

### Dependencies
* Any modern browser (i.e. Firefox, Chrome, Edge, Safari)
* A production Jira environment
* A test Jira environment

### Installation

#### Method 1: Click and drag
1. Drag one of the following links onto your bookmarks bar
   * Open new tab: <a href="javascript: (() => {    if (window.location.hostname == 'test-instance.atlassian.net') {        window.open(window.location.href.replace('test-instance.atlassian.net', 'prod-instance.atlassian.net'))    } else if (window.location.hostname == 'prod-instance.atlassian.net') {        window.open(window.location.href.replace('prod-instance.atlassian.net', 'test-instance.atlassian.net'))    } else {        alert('Error: Unexpected URL.')    }})();">Switch Env</a>
   * Open in same tab: <a href="javascript: (() => {    if (window.location.hostname == 'test-instance.atlassian.net') {        window.open(window.location.href.replace('test-instance.atlassian.net', 'prod-instance.atlassian.net'), '_self')    } else if (window.location.hostname == 'test-instance.atlassian.net') {        window.open(window.location.href.replace('prod-instance.atlassian.net', 'test-instance.atlassian.net'), '_self')    } else {        alert('Error: Unexpected URL.')    }})();">Switch Env</a>
2. If the above link does not show, go [here](https://kevyuan.github.io/jira-environment-switcher/) first
3. Modify the URLs for use with your environments

#### Method 2: Manually create new bookmark
1. Create a new bookmark using one of the following code blocks:

To open a new tab:
```
javascript: (() => {
    if (window.location.hostname == 'test-instance.atlassian.net') {
        window.open(window.location.href.replace('test-instance.atlassian.net', 'prod-instance.atlassian.net'))
    } else if (window.location.hostname == 'prod-instance.atlassian.net') {
        window.open(window.location.href.replace('prod-instance.atlassian.net', 'test-instance.atlassian.net'))
    } else {
        alert('Error: Unexpected URL.')
    }
})();
```

To open in the same tab:
```
javascript: (() => {
    if (window.location.hostname == 'test-instance.atlassian.net') {
        window.open(window.location.href.replace('test-instance.atlassian.net', 'prod-instance.atlassian.net'), '_self')
    } else if (window.location.hostname == 'prod-instance.atlassian.net') {
        window.open(window.location.href.replace('prod-instance.atlassian.net', 'test-instance.atlassian.net'), '_self')
    } else {
        alert('Error: Unexpected URL.')
    }
})();
```

2. Modify the URLs for use with your environments

## Usage
1. Go to a https://prod-instance.atlassian.net/jira/your-work
2. Click on the bookmarklet

## License
Distributed under the Apache-2.0 License. See the 'LICENSE' for more information.
