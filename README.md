# Q-SYS Browser Lite

A lightweight HTTP browser plugin for Q-SYS that can fetch web pages, manage authentication flows, extract content, and display images — all from within the Q-SYS ecosystem.

## Features

- **HTTP/HTTPS Requests** — GET, POST, PUT, DELETE, PATCH with custom headers and body
- **Navigation** — URL bar with back/forward/refresh history controls
- **HTML Parsing** — Extracts page title, text content, links, and images from HTML
- **Image Display** — Renders up to 4 images from the page via Media Display controls
- **Link Navigation** — Browse extracted links via dropdown selector
- **Cookie Management** — Automatic cookie handling with persistence across reboots
- **Authentication** — Built-in support for Basic Auth and Form-based login
- **Redirect Following** — Automatically follows 301/302/303/307/308 redirects
- **JSON Pretty-Print** — Detects JSON responses and formats them for readability
- **Custom Headers** — Send custom HTTP headers with any request
- **Response Inspector** — View response headers, status codes, and content types

## Plugin Pages

### 1. Browser
Main interface with URL bar, navigation buttons, page content display, link dropdown, and image thumbnails.

### 2. Auth
Configure authentication type (None/Basic/Form), credentials, login URL, and view/clear cookies.

### 3. Request
Advanced request configuration — HTTP method, custom headers (JSON), request body, and response header inspector.

## Properties

| Property | Type | Default | Description |
|---|---|---|---|
| User Agent | String | `QSys-Browser-Lite/0.1` | User agent sent with requests |
| Request Timeout | Integer | 10 | HTTP request timeout in seconds |
| Max Redirects | Integer | 5 | Maximum redirect hops to follow |
| Core IP Address | String | (empty) | Core IP for OAuth redirect server |

## Installation

1. Copy `QSys_Browser_Lite.qplug` to your Q-SYS Designer plugins directory
2. In Q-SYS Designer, add the plugin to your design
3. Configure properties as needed
4. Deploy to your Core

## Usage

### Basic Browsing
1. Enter a URL in the URL bar (e.g., `https://httpbin.org/html`)
2. Press **Go** or hit Enter
3. View extracted content in the Page Content area
4. Browse links via the Links dropdown, click **Go** to navigate

### Basic Auth
1. Go to the **Auth** page
2. Set Auth Type to **Basic**
3. Enter username and password
4. Navigate to the protected URL

### Form Login
1. Go to the **Auth** page
2. Set Auth Type to **Form**
3. Enter username, password, and the login form URL
4. The plugin will POST credentials and capture session cookies
5. Subsequent requests will include the session cookies

## Author

Dustin Bennett — [TEL Systems](https://github.com/Sequence32)

## License

MIT
