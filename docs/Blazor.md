

Blazor Notes
October 2019 
CSHood

Blazor is a single page web app framework that runs in the browser via Web Assembly.  
based on C#, Razor and HTML.  
The name is an amalgamation of:  Browser + Razor.   Blazor!
Instead of JavaScript to build composable web UI, you use C# and Razor syntax


Blazor will have all the features of a modern web framework including:
A component model for building composable UI
Routing
Layouts
Forms and validation
Dependency injection
JavaScript interop
Live reloading in the browser during development
Server-side rendering
Full .NET debugging both in browsers and in the IDE
Rich IntelliSense and tooling
Ability to run on older (non-WebAssembly) browsers via asm.js
Publishing and app size trimming

WebAssembly changes the Web  (WASM)
Running .NET in the browser is made possible by WebAssembly, a new web standard for a “portable, size- and load-time-efficient format suitable for compilation to the web.” WebAssembly enables fundamentally new ways to write web apps. Code compiled to WebAssembly can run in any browser at native speeds. This is the foundational piece needed to build a .NET runtime that can run in the browser. No plugins or transpilation needed. You run normal .NET assemblies in the browser using a WebAssembly based .NET runtime.


there are 2 hosting models:
Client side- 
runs on a WebAssembly-based .Net runtime (Blazor WebAssembly)
The Blazor app, its dependencies, and the .NET runtime are downloaded to the browser.
the app is executed directly on the browser UI thread.  
Updates and event handling occur within the same process.
the app’s assets are deployed as static files to a web server or service capable of serving static content to clients.
to create in the .NET Core CLI:  dotnet new blazorwasm -o <myWebAppName>  


Server side
runs in ASP.NET Core (Blazor Server)








