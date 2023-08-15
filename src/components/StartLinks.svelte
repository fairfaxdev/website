<script>

</script>

<ul class="startlinks">
    <li class="icon"><img src="http://www.htmldrive.net/edit_media/2010/201007/20100712/win7startmenu/folder.png" alt=""></li>
    <li><span>Documents</span></li>
    <li><span>Pictures</span></li>
    <li><span>Music</span></li>
    <li><span>Computer</span></li>
    <li><span>Network</span></li>
    <li><span>Connect to</span></li>
</ul>

<style lang="scss">
    :root {
        --link-radius: 3px;
        --taskbar-background: linear-gradient( to top, rgba(21,22,24,.9) 0%, rgba(27,28,30,.9) 49%, rgba(73,74,76,.9) 50%, rgba(135,142,135,.9) 95%, rgba(184,178,180,.9) 96%, rgba(184,178,180,.9) 99%, rgba(27,28,30,.9) 100% );
    }
    .startlinks {
        float:left; 
        display:block; 
        padding:0; 
        list-style:none;
        margin:7px; 
        margin-top:-30px;
        
        & li.icon {
            text-align:center;
        }
        
        & li {
            border:solid 1px transparent;
            display:block;
            margin:5px 0;
            position:relative;
            color:#fff;
            text-decoration:none;
            min-width:120px;
            user-select: none;
        }
        
        & li:not(:first-child) {
            padding: 5px;
            cursor: default;
        }
        & li:not(:first-child):hover {
            border:solid 1px #000;
            border-radius:var(--link-radius);
            box-shadow: 0 0 1px #fff; -moz-box-shadow: inset 0 0 1px #fff; -webkit-box-shadow: inset 0 0 1px #fff;
            background-image: var(--taskbar-background);
        }
    }

</style>