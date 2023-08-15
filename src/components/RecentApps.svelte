<script>
    import InternetExplorer from "../icons/InternetExplorer.svelte";
    import VisualStudio from "../icons/VisualStudio.svelte";
</script>

<ul class="recentapps">
    <li><VisualStudio />Visual Studio Code</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/chrome.png" alt="">Google Chrome</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/safari.png" alt="">Safari</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/opera.png" alt="">Opera</li>
    <li><InternetExplorer />Internet Explorer</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/rss_32.png" alt="">RSS Feeds</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/twitter_32.png" alt="">Twitter</li>
    <li><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/delicious_32.png" alt="">Delicious</li>
</ul>

<style>
    :root {
        --apps-radius: 3px;
    }
    .recentapps {
        float:left; 
        display:block; 
        padding:0; 
        list-style:none;
    }
    .recentapps {
        background: var(--surface); 
        border: solid 1px rgba(0,0,0,.7); 
        margin: 7px 0 7px 7px;
        box-shadow: 0 0 1px #fff;
        border-radius: var(--apps-radius);
        & li { 
            border: solid 1px transparent; 
            display: block; 
            padding: 3px; 
            margin: 3px;
            color: #4b4b4b; 
            text-decoration: none;
            user-select: none;
            min-width: 220px;
            cursor: default;
        }
        & li:hover {
            border: solid 1px #7da2ce;
            border-radius: var(--apps-radius);
            box-shadow: inset 0 0 1px #fff;
            background-color: #cfe3fd;
            background: linear-gradient(to top, #dcebfd, #c2dcfd);
        }
        & li img, & li svg {
            border: 0;
            vertical-align: middle;
            margin: 0 5px 0 0;
        }
        & li svg {
            max-width: 30px;
            max-height: 30px;
        }
    }
</style>