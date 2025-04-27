---
id: "104b26a2-cf3c-4d61-9e56-95f00e56e5bc"
title: "gracefully close apps"
created: "2025-04-26T19:36:39.972404+00:00"
updated: "2025-04-26T19:36:48.924414+00:00"
notebook: "Terminal commands"
section: "New Section"
item: "New Item"
---

<p>osascript -e '</p><p>tell application "System Events"</p><p>    set runningApps to name of every application process where background only is false</p><p>end tell</p><p>-- Close all applications except Terminal and Finder</p><p>repeat with appName in runningApps</p><p>    if appName is not "Terminal" and appName is not "Finder" then</p><p>        try</p><p>            tell application appName</p><p>                quit</p><p>            end tell</p><p>        end try</p><p>    end if</p><p>end repeat</p><p>-- Close all Finder windows without quitting Finder</p><p>tell application "Finder"</p><p>    close every window</p><p>end tell</p><p>'</p>