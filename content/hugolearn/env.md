
HUGO_ENV = "development"
########################### DEV
    {{ if eq (getenv "HUGO_ENV") "development" }}
    <!-- dev stuff here -->


    baseURL = "localhost:1313"
    title = "LOCAL: "

    {{ end }}
########################### STAGING
{{ if eq (getenv "HUGO_ENV") "staging" }}
<!-- staging stuff here -->

baseURL = "https://stage-sakumatto-fi.firebaseapp.com"
title = "STAGING: Holistinen katsaus yhteiskuntaan ja elämään sekä puheenvuoro jakamisen periaatteen puolesta"
disqusShortname = "sakumatto"

{{ end }}
########################### PRODUCTION
{{ if eq (getenv "HUGO_ENV") "production" }}
<!-- production stuff here -->

baseURL = "https://sakumatto.fi"
title = "Holistinen katsaus yhteiskuntaan ja elämään sekä puheenvuoro jakamisen periaatteen puolesta"
disqusShortname = "sakumatto"
googleAnalytics = "UA-26834518-1"

{{ end }}
############################
