---
layout: single
title: Last automated build
---

Download the latest Gyroflow development build generated from [GitHub Actions](https://github.com/gyroflow/gyroflow/actions).

Link to this page with auto-download: `https://gyroflow.xyz/devbuild/?autodownload`

<a id="buildbtn" href="https://nightly.link/gyroflow/gyroflow/workflows/release/master/gyroflow.zip" class="btn btn--info btn--large">Download last build</a>

<script type="text/javascript">

    document.addEventListener("DOMContentLoaded", function() {
        
		$('a#someID').attr({target: '_blank', 
                    href  : 'https://nightly.link/gyroflow/gyroflow/workflows/release/master/gyroflow.zip'});

        $.getJSON( "https://api.github.com/repos/gyroflow/gyroflow/actions/artifacts", function( data ) {
          var lastbuild = data.artifacts[0];
          console.log(lastbuild);
          $("#buildbtn").text("Download last build: " + lastbuild.created_at + " (" + Math.round(lastbuild.size_in_bytes/1e6)+ "MB)");

        });

        if (window.location.href.split("?")[1] == "autodownload") {
        	setTimeout(function() {
        	   window.location.href = "https://nightly.link/gyroflow/gyroflow/workflows/release/master/gyroflow.zip"
        	}, 1000);

        }
    });

</script>