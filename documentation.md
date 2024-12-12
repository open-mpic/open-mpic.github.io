---
title: Open MPIC API Documentation
classes: wide
layout: single
---
<!--<redoc spec-url="https://raw.githubusercontent.com/open-mpic/open-mpic-specification/main/openapi.yaml"></redoc>-->
<redoc id="spec-elem"></redoc>

<script type="text/javascript">
        const params = new URLSearchParams(window.location.search);
        var commit = params.get('commit');
        var spec_url = null;
        if (commit !== null) {
            spec_url = "https://raw.githubusercontent.com/open-mpic/open-mpic-specification/" + commit + "/openapi.yaml";
        } else {
            spec_url = "https://raw.githubusercontent.com/open-mpic/open-mpic-specification/main/openapi.yaml";
        }
        var spec_elem = document.getElementById("spec-elem");
        spec_elem.setAttribute("spec-url", spec_url);

</script>

<script src="https://cdn.redoc.ly/redoc/latest/bundles/redoc.standalone.js"> </script>


