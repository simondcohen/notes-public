---
id: "f0ee4f3b-2584-430d-bebe-231f494060af"
title: "New Note"
created: "2025-04-23T20:13:10.384858+00:00"
updated: "2025-04-23T23:05:30.583232+00:00"
notebook: "Web dev notes"
section: "Task manager app"
item: "Json import format"
---

<h3>JSON template (copy-paste as is)</h3><p>{ "todos": [ { "id": 42, "text": "Read Adorno chapter-3", "deadline": "2025-05-10", "time": null, "completed": false, "category": "reading" } ], "deadlines": [ { "id": "prospectus", "title": "Dissertation prospectus", "dueDate": "2025-05-28", "notes": "", "completed": false } ] }</p><hr><h3>How to read it</h3><ul><li><p><strong>Root level</strong> – two lists:<br>• <code>"todos"</code> – day-to-day tasks.<br>• <code>"deadlines"</code> – bigger items you track on the timeline.</p></li><li><p><strong>Every item needs an </strong><code>"id"</code><br>Use any unique string or number. Matching an existing id updates that item; a brand-new id creates a new one.</p></li><li><p><strong>Typical task fields</strong><br>• <code>"text"</code> – what you need to do.<br>• <code>"deadline"</code> (date) and <code>"time"</code> (optional clock time).<br>• <code>"completed": true</code> marks it done.<br>• <code>"category"</code> keeps things grouped (e.g. “reading”, “errand”).</p></li><li><p><strong>Typical deadline fields</strong><br>• <code>"title"</code> – short label.<br>• <code>"dueDate"</code> – date the deadline is due.<br>• <code>"notes"</code> – anything extra you want to remember.<br>• <code>"completed"</code> – same idea as above.</p></li></ul><p>Feel free to add or omit optional fields (like <code>notes</code> or <code>time</code>)—the app will ignore anything it doesn’t recognise, and only the fields you include will be imported or updated.</p>