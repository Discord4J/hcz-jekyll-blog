---
layout: page
title: Javadocs
permalink: /docs
---
<section class="page-header">
    <h1 class="project-name">Discord4J Javadocs</h1>
    <p><p></p></p>
    <div id="buttons">
        <script type="text/javascript">
                var btn = document.createElement("a");
                btn.setAttribute("href", "http://austinv11.github.io/Discord4J/latestdoc.html");
                btn.setAttribute("class", "btn");
                btn.innerHTML = "Latest Stable Version Javadoc";
                document.getElementById("buttons").appendChild(btn);
            </script>
        <a href="https://jitpack.io/com/github/austinv11/Discord4j/dev-SNAPSHOT/javadoc/" class="btn">Latest Development Version Javadoc</a>
    </div>
</section>

<section class="main-content">
    <p>Listed below are the links to the online version of the associated release's javadoc:</p>
    <script type="text/javascript">
            //alert("test");
            var rawFile = new XMLHttpRequest();
            rawFile.open("GET", "https://api.github.com/repos/austinv11/Discord4j/releases", true);
            rawFile.onreadystatechange = function () {
                var list = document.createElement("ul");
                document.getElementById("list").appendChild(list);
                if(rawFile.readyState === 4) {
                    if(rawFile.status === 200 || rawFile.status == 0) {
                        var releases = JSON.parse(rawFile.responseText)
                        for (i = 0; i < releases.length; i++) {
                            var release = releases[i]
                            var version = release.tag_name
                             var btn = document.createElement("li");
                             btn.innerHTML = "<a href=https://jitpack.io/com/github/austinv11/Discord4j/"+version+"/javadoc/>"+version+"</a>"
                             list.appendChild(btn);
                        }
                    }
                }
            }
            rawFile.send(null);
        </script>
    <div id="list">

    </div>
</section>