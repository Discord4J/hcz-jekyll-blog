---
layout: page
title: Downloads
permalink: /downloads.html
---

<section class="page-header">
    <h1 class="project-name">Discord4J Direct Downloads</h1>
</section>

<section class="main-content">
    <p>Below are direct download links to Discord4J .jar files:</p>
    <p>If you want to get the jar with all the D4J dependencies included (you usually want this), click on <strong>Shaded</strong>.</p>
    <script type="text/javascript">
        //alert("test");
        var rawFile = new XMLHttpRequest();
        rawFile.open("GET", "https://api.github.com/repos/Discord4J/Discord4J/releases", true);
        rawFile.onreadystatechange = function () {
            var list = document.createElement("ul");
            document.getElementById("list").appendChild(list);
            if(rawFile.readyState === 4) {
                if(rawFile.status === 200 || rawFile.status == 0) {
                    var snapshotBtn = document.createElement("li");
                    snapshotBtn.innerHTML = "<a href=https://jitpack.io/com/github/Discord4J/Discord4J/dev-SNAPSHOT/Discord4J-dev-SNAPSHOT.jar>Latest Development (Unstable) Build</a> (<strong><a href=https://jitpack.io/com/github/Discord4J/Discord4J/dev-SNAPSHOT/Discord4J-dev-SNAPSHOT-shaded.jar>Shaded</a></strong>, <a href=https://jitpack.io/com/github/austinv11/Discord4J/dev-SNAPSHOT/Discord4J-dev-SNAPSHOT-javadoc.jar>Javadoc</a>, <a href=https://jitpack.io/com/github/Discord4J/Discord4J/dev-SNAPSHOT/Discord4J-dev-SNAPSHOT-sources.jar>Source</a>)"
                    list.appendChild(snapshotBtn);
                    var releases = JSON.parse(rawFile.responseText)
                    for (i = 0; i < releases.length; i++) {
                        var release = releases[i]
                        var version = release.tag_name
                        var btn = document.createElement("li");
                        btn.innerHTML = "<a href=https://jitpack.io/com/github/Discord4J/Discord4J/"+version+"/Discord4J-"+version+".jar>"+version+"</a> (<strong><a href=https://jitpack.io/com/github/Discord4J/Discord4J/"+version+"/Discord4J-"+version+"-shaded.jar>Shaded</a></strong>, <a href=https://jitpack.io/com/github/Discord4J/Discord4J/"+version+"/Discord4J-"+version+"-javadoc.jar>Javadoc</a>, <a href=https://jitpack.io/com/github/Discord4J/Discord4J/"+version+"/Discord4J-"+version+"-sources.jar>Source</a>)"
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
