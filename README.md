# core-apps-meta
Meta app for all core apps

This app is a little tricky, and should rarely matter. But when it matters, it can be very useful.

This app enumerates all core apps (and their versions) in its <Cytoscape-App-Dependencies> tag. Its sole purpose is to cause all of those apps to be downloaded as a side effect of downloading this app from the app store. This normally wouldn't matter, as the core apps are delivered with Cytoscape itself, and when a new version of a core app is checked into the app store, Cytoscape will automatically pick it up and offer it to the user.

This app's purpose is to allow additional core apps to be added to Cytoscape even after Cytoscape has already been installed. To make this happen, we add additional core apps to the <Cytoscape-App-Dependencies> tag, bump this app's version, and check it into the app store. Because it has a higher version than the one delivered with Cytoscape, it will be offered to the user when Cytoscape starts up. If the user allows it to be downloaded, it will drag the new core app with it (as a dependency).

Viola ... new core apps can be delivered even after Cytoscape is released and installed.

Note that this is useful for delivering a core app that wasn't ready at release time, but is still fundamental to some concept of Cytoscape.

