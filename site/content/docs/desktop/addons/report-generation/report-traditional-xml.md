---
# This page was generated from the add-on.
title: Traditional XML Report
type: userguide
---

# Traditional XML Report

### Sample

```
<?xml version="1.0"?>
<OWASPZAPReport version="Dev Build" generated="Fri, 4 Feb 2022 17:42:18">
    
        <site name="http://localhost:8080" host="localhost" port="8080" ssl="false">
            <alerts>

                    <alertitem>
                        <pluginid>20012</pluginid>
                        <alertRef>20012</alertRef>
                        <alert>Anti-CSRF Tokens Check</alert>
                        <name>Anti-CSRF Tokens Check</name>
                        <riskcode>3</riskcode>
                        <confidence>2</confidence>
                        <riskdesc>High (Medium)</riskdesc>
                        <confidencedesc>Medium</confidencedesc>
                        <desc><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge...</desc>
                        <instances>

                                <instance>
                                    <uri>http://localhost:8080/bodgeit/advanced.jsp</uri>
                                    <method>GET</method>
                                    <param></param>
                                    <attack></attack>
                                    <evidence><form id="advanced" name="advanced" method="POST" onsubmit="return validateForm(this);false;"></evidence>
                                </instance>

                                <instance>
                                    <uri>http://localhost:8080/bodgeit/advanced.jsp</uri>
                                    <method>GET</method>
                                    <param></param>
                                    <attack></attack>
                                    <evidence><form id="query" name="advanced" method="POST"></evidence>
                                </instance>

                                <instance>
                                    <uri>http://localhost:8080/bodgeit/basket.jsp</uri>
                                    <method>GET</method>
                                    <param></param>
                                    <attack></attack>
                                    <evidence><form action="basket.jsp" method="post"></evidence>
                                </instance>


```
