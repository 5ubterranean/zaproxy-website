---
# This page was generated from the add-on.
title: Traditional JSON Report
type: userguide
---

# Traditional JSON Report

### Sample

#### About riskdesc

riskdesc - Is a combination identifier, showing Risk followed by Confidence (in brackets). For example `High (Medium)` would indicate a High risk issue identified with Medium confidence.

```
{
    "@version": "Dev Build",
    "@generated": "Fri, 4 Feb 2022 13:04:51",
    "site":[
        {
            "@name": "http://localhost:8080",
            "@host": "localhost",
            "@port": "8080",
            "@ssl": "false",
            "alerts": [
                {
                    "pluginid": "40012",
                    "alertRef": "40012",
                    "alert": "Cross Site Scripting (Reflected)",
                    "name": "Cross Site Scripting (Reflected)",
                    "riskcode": "3",
                    "confidence": "2",
                    "riskdesc": "High (Medium)",
                    "desc": "<p>Cross-site Scripting (XSS) is an attack technique that involves ...</p>",
                    "instances":[
                        {
                            "uri": "http://localhost:8080/bodgeit/search.jsp?q=%3C%2Ffont%3E%3CscrIpt%3Ealert%281%29%3B%3C%2FscRipt%3E%3Cfont%3E",
                            "method": "GET",
                            "param": "q",
                            "attack": "</font><scrIpt>alert(1);</scRipt><font>",
                            "evidence": "</font><scrIpt>alert(1);</scRipt><font>"
                        },
                        {
                            "uri": "http://localhost:8080/bodgeit/contact.jsp",
                            "method": "POST",
                            "param": "comments",
                            "attack": "</td><scrIpt>alert(1);</scRipt><td>",
                            "evidence": "</td><scrIpt>alert(1);</scRipt><td>"
                        }
                    ],                   
                    "count": "2", 
                    "solution": "<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not ...</p>",
                    "otherinfo": "",
                    "reference": "<p>http://projects.webappsec.org/Cross-Site-Scripting</p><p>http://cwe.mitre.org/data/definitions/79.html</p>",
                    "cweid": "79",
                    "wascid": "8",
                    "sourceid": "36977"
                },

```
