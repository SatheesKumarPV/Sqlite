



<!DOCTYPE html>
<html lang="en" class=" is-copy-enabled">
  <head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb# object: http://ogp.me/ns/object# article: http://ogp.me/ns/article# profile: http://ogp.me/ns/profile#">
    <meta charset='utf-8'>

    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/frameworks-ce3c74f5c71958d8d02d5f36275809f5f6e20e5244cb38e36fd299a3cb49716a.css" integrity="sha256-zjx09ccZWNjQLV82J1gJ9fbiDlJEyzjjb9KZo8tJcWo=" media="all" rel="stylesheet" />
    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/github-4d8d7740603718bde2c83ff766bf53c39972f4f6f5509c013a08497a75799732.css" integrity="sha256-TY13QGA3GL3iyD/3Zr9Tw5ly9Pb1UJwBOghJenV5lzI=" media="all" rel="stylesheet" />
    
    
    
    

    <link as="script" href="https://assets-cdn.github.com/assets/frameworks-e76ce42ce77c934586f7cacbe24d556dbe6fefdbe8b53a393644b18199f7c291.js" rel="preload" />
    
    <link as="script" href="https://assets-cdn.github.com/assets/github-3403611476aba5449f7af712dbf7b488bbb552e0a3e93c55d36c058fe7968b46.js" rel="preload" />

    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="Content-Language" content="en">
    <meta name="viewport" content="width=device-width">
    
    
    <title>Cordova-sqlite-storage/SQLitePlugin.coffee.md at storage-master · litehelpers/Cordova-sqlite-storage</title>
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
    <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
    <link rel="apple-touch-icon" href="/apple-touch-icon.png">
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57x57.png">
    <link rel="apple-touch-icon" sizes="60x60" href="/apple-touch-icon-60x60.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="76x76" href="/apple-touch-icon-76x76.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114x114.png">
    <link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon-120x120.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144x144.png">
    <link rel="apple-touch-icon" sizes="152x152" href="/apple-touch-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
    <meta property="fb:app_id" content="1401488693436528">

      <meta content="https://avatars3.githubusercontent.com/u/5294634?v=3&amp;s=400" name="twitter:image:src" /><meta content="@github" name="twitter:site" /><meta content="summary" name="twitter:card" /><meta content="litehelpers/Cordova-sqlite-storage" name="twitter:title" /><meta content="Cordova-sqlite-storage - A Cordova/PhoneGap plugin to open and use sqlite databases on Android &amp; iOS with HTML5/Web SQL API (Windows version available)" name="twitter:description" />
      <meta content="https://avatars3.githubusercontent.com/u/5294634?v=3&amp;s=400" property="og:image" /><meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="litehelpers/Cordova-sqlite-storage" property="og:title" /><meta content="https://github.com/litehelpers/Cordova-sqlite-storage" property="og:url" /><meta content="Cordova-sqlite-storage - A Cordova/PhoneGap plugin to open and use sqlite databases on Android &amp; iOS with HTML5/Web SQL API (Windows version available)" property="og:description" />
      <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">
    <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">
    <link rel="assets" href="https://assets-cdn.github.com/">
    <link rel="web-socket" href="wss://live.github.com/_sockets/MTg3MTQxMDg6YzhmM2VhMzNlMjJmZDg0NWEzMjRjMWUxYmIyNTU2MTk6NjU2NDE0MmMzNTQxOGE5MGU0Yjc0NjE5ODA3ZWVhZTQ2MzhlNzBjM2M5YmYwNDJkZWE2NjYzMTY2YWZiYzhlOQ==--f5109744c017045eaf7b86ea757113c6e8f8c9ca">
    <meta name="pjax-timeout" content="1000">
    <link rel="sudo-modal" href="/sessions/sudo_modal">

    <meta name="msapplication-TileImage" content="/windows-tile.png">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="selected-link" value="repo_source" data-pjax-transient>

    <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
<meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-analytics" content="UA-3769691-2">

<meta content="collector.githubapp.com" name="octolytics-host" /><meta content="github" name="octolytics-app-id" /><meta content="DCE1D22D:8521:147D2323:57467E14" name="octolytics-dimension-request_id" /><meta content="18714108" name="octolytics-actor-id" /><meta content="SatheesKumarPV" name="octolytics-actor-login" /><meta content="9a74fdb7a51c605ccd040210ad77b1b9ed5e55c0463cf9bec94de62658c0e472" name="octolytics-actor-hash" />
<meta content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" name="analytics-location" />



  <meta class="js-ga-set" name="dimension1" content="Logged In">



        <meta name="hostname" content="github.com">
    <meta name="user-login" content="SatheesKumarPV">

        <meta name="expected-hostname" content="github.com">
      <meta name="js-proxy-site-detection-payload" content="MTZhNTBkZTUxZWIwYWI5ZjVkYWZmOTA4Y2NjZWE2ZmIxNWM3NTAyZTdkYzMyOTMxOWIwMDM5ZGFhMzljZDE4Y3x7InJlbW90ZV9hZGRyZXNzIjoiMjIwLjIyNS4yMTAuNDUiLCJyZXF1ZXN0X2lkIjoiRENFMUQyMkQ6ODUyMToxNDdEMjMyMzo1NzQ2N0UxNCIsInRpbWVzdGFtcCI6MTQ2NDIzNzU5NH0=">


      <link rel="mask-icon" href="https://assets-cdn.github.com/pinned-octocat.svg" color="#4078c0">
      <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">

    <meta name="html-safe-nonce" content="338a831cd251dadca6ea5444e9f00f52f8106199">
    <meta content="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" name="form-nonce" />

    <meta http-equiv="x-pjax-version" content="28e6c1aea7b458688812e600c223f2e1">
    

      
  <meta name="description" content="Cordova-sqlite-storage - A Cordova/PhoneGap plugin to open and use sqlite databases on Android &amp; iOS with HTML5/Web SQL API (Windows version available)">
  <meta name="go-import" content="github.com/litehelpers/Cordova-sqlite-storage git https://github.com/litehelpers/Cordova-sqlite-storage.git">

  <meta content="5294634" name="octolytics-dimension-user_id" /><meta content="litehelpers" name="octolytics-dimension-user_login" /><meta content="10120864" name="octolytics-dimension-repository_id" /><meta content="litehelpers/Cordova-sqlite-storage" name="octolytics-dimension-repository_nwo" /><meta content="true" name="octolytics-dimension-repository_public" /><meta content="false" name="octolytics-dimension-repository_is_fork" /><meta content="10120864" name="octolytics-dimension-repository_network_root_id" /><meta content="litehelpers/Cordova-sqlite-storage" name="octolytics-dimension-repository_network_root_nwo" />
  <link href="https://github.com/litehelpers/Cordova-sqlite-storage/commits/storage-master.atom" rel="alternate" title="Recent Commits to Cordova-sqlite-storage:storage-master" type="application/atom+xml">


      <link rel="canonical" href="https://github.com/litehelpers/Cordova-sqlite-storage/blob/storage-master/SQLitePlugin.coffee.md" data-pjax-transient>
  </head>


  <body class="logged-in   env-production windows vis-public page-blob">
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"></div>
    <a href="#start-of-content" tabindex="1" class="accessibility-aid js-skip-to-content">Skip to content</a>

    
    
    



        <div class="header header-logged-in true" role="banner">
  <div class="container clearfix">

    <a class="header-logo-invertocat" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg aria-hidden="true" class="octicon octicon-mark-github" height="28" version="1.1" viewBox="0 0 16 16" width="28"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59 0.4 0.07 0.55-0.17 0.55-0.38 0-0.19-0.01-0.82-0.01-1.49-2.01 0.37-2.53-0.49-2.69-0.94-0.09-0.23-0.48-0.94-0.82-1.13-0.28-0.15-0.68-0.52-0.01-0.53 0.63-0.01 1.08 0.58 1.23 0.82 0.72 1.21 1.87 0.87 2.33 0.66 0.07-0.52 0.28-0.87 0.51-1.07-1.78-0.2-3.64-0.89-3.64-3.95 0-0.87 0.31-1.59 0.82-2.15-0.08-0.2-0.36-1.02 0.08-2.12 0 0 0.67-0.21 2.2 0.82 0.64-0.18 1.32-0.27 2-0.27 0.68 0 1.36 0.09 2 0.27 1.53-1.04 2.2-0.82 2.2-0.82 0.44 1.1 0.16 1.92 0.08 2.12 0.51 0.56 0.82 1.27 0.82 2.15 0 3.07-1.87 3.75-3.65 3.95 0.29 0.25 0.54 0.73 0.54 1.48 0 1.07-0.01 1.93-0.01 2.2 0 0.21 0.15 0.46 0.55 0.38C13.71 14.53 16 11.53 16 8 16 3.58 12.42 0 8 0z"></path></svg>
</a>


        <div class="header-search scoped-search site-scoped-search js-site-search" role="search">
  <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/search" class="js-site-search-form" data-scoped-search-url="/litehelpers/Cordova-sqlite-storage/search" data-unscoped-search-url="/search" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <label class="form-control header-search-wrapper js-chromeless-input-container">
      <div class="header-search-scope">This repository</div>
      <input type="text"
        class="form-control header-search-input js-site-search-focus js-site-search-field is-clearable"
        data-hotkey="s"
        name="q"
        placeholder="Search"
        aria-label="Search this repository"
        data-unscoped-placeholder="Search GitHub"
        data-scoped-placeholder="Search"
        tabindex="1"
        autocapitalize="off">
    </label>
</form></div>


      <ul class="header-nav left" role="navigation">
        <li class="header-nav-item">
          <a href="/pulls" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:pulls context:user" data-hotkey="g p" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls">
            Pull requests
</a>        </li>
        <li class="header-nav-item">
          <a href="/issues" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:issues context:user" data-hotkey="g i" data-selected-links="/issues /issues/assigned /issues/mentioned /issues">
            Issues
</a>        </li>
          <li class="header-nav-item">
            <a class="header-nav-link" href="https://gist.github.com/" data-ga-click="Header, go to gist, text:gist">Gist</a>
          </li>
      </ul>

    
<ul class="header-nav user-nav right" id="user-links">
  <li class="header-nav-item">
    

  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link tooltipped tooltipped-s js-menu-target" href="/new"
       aria-label="Create new…"
       data-ga-click="Header, create new, icon:add">
      <svg aria-hidden="true" class="octicon octicon-plus left" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 9H7v5H5V9H0V7h5V2h2v5h5v2z"></path></svg>
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <ul class="dropdown-menu dropdown-menu-sw">
        
<a class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>


  <a class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>



  <div class="dropdown-divider"></div>
  <div class="dropdown-header">
    <span title="litehelpers/Cordova-sqlite-storage">This repository</span>
  </div>
    <a class="dropdown-item" href="/litehelpers/Cordova-sqlite-storage/issues/new" data-ga-click="Header, create new issue">
      New issue
    </a>

      </ul>
    </div>
  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link name tooltipped tooltipped-sw js-menu-target" href="/SatheesKumarPV"
       aria-label="View profile and more"
       data-ga-click="Header, show menu, icon:avatar">
      <img alt="@SatheesKumarPV" class="avatar" height="20" src="https://avatars3.githubusercontent.com/u/18714108?v=3&amp;s=40" width="20" />
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <div class="dropdown-menu  dropdown-menu-sw">
        <div class=" dropdown-header header-nav-current-user css-truncate">
            Signed in as <strong class="css-truncate-target">SatheesKumarPV</strong>

        </div>


        <div class="dropdown-divider"></div>

          <a class="dropdown-item" href="/SatheesKumarPV" data-ga-click="Header, go to profile, text:your profile">
            Your profile
          </a>
        <a class="dropdown-item" href="/stars" data-ga-click="Header, go to starred repos, text:your stars">
          Your stars
        </a>
          <a class="dropdown-item" href="/explore" data-ga-click="Header, go to explore, text:explore">
            Explore
          </a>
          <a class="dropdown-item" href="/integrations" data-ga-click="Header, go to integrations, text:integrations">
            Integrations
          </a>
        <a class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">
          Help
        </a>


          <div class="dropdown-divider"></div>

          <a class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">
            Settings
          </a>

          <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/logout" class="logout-form" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="9VMy0FAE6vtj7eCDrQGks+TQTP9r/UTMDc/AsjT+vnsUg1E3nf5y1efc2NFEJkT2Nk94AiijzXhSiedxO8Gw0A==" /></div>
            <button class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout">
              Sign out
            </button>
</form>
      </div>
    </div>
  </li>
</ul>


    
  </div>
</div>


      


    <div id="start-of-content" class="accessibility-aid"></div>

      <div id="js-flash-container">
</div>


    <div role="main" class="main-content">
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode">
    <div id="js-repo-pjax-container" data-pjax-container>
      
<div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav">
  <div class="container repohead-details-container">

    

<ul class="pagehead-actions">

  <li>
        <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/notifications/subscribe" class="js-social-container" data-autosubmit="true" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="mDsZNvIgogCp0vH6PEU3Qp7HhonCJ6KXA37fZMQAzlMQmAlerPOLxfF8DZI47HUK/K0VGkm782glKLvjA6r10A==" /></div>      <input class="form-control" id="repository_id" name="repository_id" type="hidden" value="10120864" />

        <div class="select-menu js-menu-container js-select-menu">
          <a href="/litehelpers/Cordova-sqlite-storage/subscription"
            class="btn btn-sm btn-with-count select-menu-button js-menu-target" role="button" tabindex="0" aria-haspopup="true"
            data-ga-click="Repository, click Watch settings, action:blob#show">
            <span class="js-select-button">
              <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6c4.94 0 7.94-6 7.94-6S13 2 8.06 2z m-0.06 10c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4z m2-4c0 1.11-0.89 2-2 2s-2-0.89-2-2 0.89-2 2-2 2 0.89 2 2z"></path></svg>
              Watch
            </span>
          </a>
          <a class="social-count js-social-count" href="/litehelpers/Cordova-sqlite-storage/watchers">
            112
          </a>

        <div class="select-menu-modal-holder">
          <div class="select-menu-modal subscription-menu-modal js-menu-content" aria-hidden="true">
            <div class="select-menu-header js-navigation-enable" tabindex="-1">
              <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48-3.75-3.75-3.75 3.75-1.48-1.48 3.75-3.75L0.77 4.25l1.48-1.48 3.75 3.75 3.75-3.75 1.48 1.48-3.75 3.75z"></path></svg>
              <span class="select-menu-title">Notifications</span>
            </div>

              <div class="select-menu-list js-navigation-container" role="menu">

                <div class="select-menu-item js-navigation-item selected" role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
                  <div class="select-menu-item-text">
                    <input checked="checked" id="do_included" name="do" type="radio" value="included" />
                    <span class="select-menu-item-heading">Not watching</span>
                    <span class="description">Be notified when participating or @mentioned.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6c4.94 0 7.94-6 7.94-6S13 2 8.06 2z m-0.06 10c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4z m2-4c0 1.11-0.89 2-2 2s-2-0.89-2-2 0.89-2 2-2 2 0.89 2 2z"></path></svg>
                      Watch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
                  <div class="select-menu-item-text">
                    <input id="do_subscribed" name="do" type="radio" value="subscribed" />
                    <span class="select-menu-item-heading">Watching</span>
                    <span class="description">Be notified of all conversations.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6c4.94 0 7.94-6 7.94-6S13 2 8.06 2z m-0.06 10c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4z m2-4c0 1.11-0.89 2-2 2s-2-0.89-2-2 0.89-2 2-2 2 0.89 2 2z"></path></svg>
                      Unwatch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
                  <div class="select-menu-item-text">
                    <input id="do_ignore" name="do" type="radio" value="ignore" />
                    <span class="select-menu-item-heading">Ignoring</span>
                    <span class="description">Never be notified.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-mute" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8 2.81v10.38c0 0.67-0.81 1-1.28 0.53L3 10H1c-0.55 0-1-0.45-1-1V7c0-0.55 0.45-1 1-1h2l3.72-3.72c0.47-0.47 1.28-0.14 1.28 0.53z m7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06 1.97 1.97-1.97 1.97 1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06-1.97-1.97 1.97-1.97z"></path></svg>
                      Stop ignoring
                    </span>
                  </div>
                </div>

              </div>

            </div>
          </div>
        </div>
</form>
  </li>

  <li>
    
  <div class="js-toggler-container js-social-container starring-container ">

    <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/unstar" class="starred" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="pYIgeCvUpZJUWLt6lDJXXjYHwcFmd8Dv8wYmAyc/FTOH01MiG/2xgSpQ7NEoi9NuoR5G/uAxl9jZr8evAYrhbg==" /></div>
      <button
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Unstar this repository" title="Unstar litehelpers/Cordova-sqlite-storage"
        data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M14 6l-4.9-0.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14l4.33-2.33 4.33 2.33L10.4 9.26 14 6z"></path></svg>
        Unstar
      </button>
        <a class="social-count js-social-count" href="/litehelpers/Cordova-sqlite-storage/stargazers">
          1,178
        </a>
</form>
    <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/star" class="unstarred" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="IFPied4pTArhqEB6yviwjwxRuEKUHkyleguJ+UriU7O5HaP3Rqb5BLpO+L4AwshpGPRtXBJ/M2x77oPW2EAg6A==" /></div>
      <button
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Star this repository" title="Star litehelpers/Cordova-sqlite-storage"
        data-ga-click="Repository, click star button, action:blob#show; text:Star">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M14 6l-4.9-0.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14l4.33-2.33 4.33 2.33L10.4 9.26 14 6z"></path></svg>
        Star
      </button>
        <a class="social-count js-social-count" href="/litehelpers/Cordova-sqlite-storage/stargazers">
          1,178
        </a>
</form>  </div>

  </li>

  <li>
          <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/fork" class="btn-with-count" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="aoUQdMI3IKqPhKX7/KnS6soecnppeh5iau52HSF6nbPBjGBOf7/5rVtV7oaTfLaDxMYaCXDafXagBBUhRjMpfg==" /></div>
            <button
                type="submit"
                class="btn btn-sm btn-with-count"
                data-ga-click="Repository, show fork modal, action:blob#show; text:Fork"
                title="Fork your own copy of litehelpers/Cordova-sqlite-storage to your account"
                aria-label="Fork your own copy of litehelpers/Cordova-sqlite-storage to your account">
              <svg aria-hidden="true" class="octicon octicon-repo-forked" height="16" version="1.1" viewBox="0 0 10 16" width="10"><path d="M8 1c-1.11 0-2 0.89-2 2 0 0.73 0.41 1.38 1 1.72v1.28L5 8 3 6v-1.28c0.59-0.34 1-0.98 1-1.72 0-1.11-0.89-2-2-2S0 1.89 0 3c0 0.73 0.41 1.38 1 1.72v1.78l3 3v1.78c-0.59 0.34-1 0.98-1 1.72 0 1.11 0.89 2 2 2s2-0.89 2-2c0-0.73-0.41-1.38-1-1.72V9.5l3-3V4.72c0.59-0.34 1-0.98 1-1.72 0-1.11-0.89-2-2-2zM2 4.2c-0.66 0-1.2-0.55-1.2-1.2s0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2-0.55 1.2-1.2 1.2z m3 10c-0.66 0-1.2-0.55-1.2-1.2s0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2-0.55 1.2-1.2 1.2z m3-10c-0.66 0-1.2-0.55-1.2-1.2s0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2-0.55 1.2-1.2 1.2z"></path></svg>
              Fork
            </button>
</form>
    <a href="/litehelpers/Cordova-sqlite-storage/network" class="social-count">
      464
    </a>
  </li>
</ul>

    <h1 class="entry-title public ">
  <svg aria-hidden="true" class="octicon octicon-repo" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M4 9h-1v-1h1v1z m0-3h-1v1h1v-1z m0-2h-1v1h1v-1z m0-2h-1v1h1v-1z m8-1v12c0 0.55-0.45 1-1 1H6v2l-1.5-1.5-1.5 1.5V14H1c-0.55 0-1-0.45-1-1V1C0 0.45 0.45 0 1 0h10c0.55 0 1 0.45 1 1z m-1 10H1v2h2v-1h3v1h5V11z m0-10H2v9h9V1z"></path></svg>
  <span class="author" itemprop="author"><a href="/litehelpers" class="url fn" rel="author">litehelpers</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a href="/litehelpers/Cordova-sqlite-storage" data-pjax="#js-repo-pjax-container">Cordova-sqlite-storage</a></strong>

</h1>

  </div>
  <div class="container">
    
<nav class="reponav js-repo-nav js-sidenav-container-pjax"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
     role="navigation"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/litehelpers/Cordova-sqlite-storage" aria-selected="true" class="js-selected-navigation-item selected reponav-item" data-hotkey="g c" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches /litehelpers/Cordova-sqlite-storage" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-code" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M9.5 3l-1.5 1.5 3.5 3.5L8 11.5l1.5 1.5 4.5-5L9.5 3zM4.5 3L0 8l4.5 5 1.5-1.5L2.5 8l3.5-3.5L4.5 3z"></path></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a href="/litehelpers/Cordova-sqlite-storage/issues" class="js-selected-navigation-item reponav-item" data-hotkey="g i" data-selected-links="repo_issues repo_labels repo_milestones /litehelpers/Cordova-sqlite-storage/issues" itemprop="url">
        <svg aria-hidden="true" class="octicon octicon-issue-opened" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7S10.14 13.7 7 13.7 1.3 11.14 1.3 8s2.56-5.7 5.7-5.7m0-1.3C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7S10.86 1 7 1z m1 3H6v5h2V4z m0 6H6v2h2V10z"></path></svg>
        <span itemprop="name">Issues</span>
        <span class="counter">149</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/litehelpers/Cordova-sqlite-storage/pulls" class="js-selected-navigation-item reponav-item" data-hotkey="g p" data-selected-links="repo_pulls /litehelpers/Cordova-sqlite-storage/pulls" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-git-pull-request" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M11 11.28c0-1.73 0-6.28 0-6.28-0.03-0.78-0.34-1.47-0.94-2.06s-1.28-0.91-2.06-0.94c0 0-1.02 0-1 0V0L4 3l3 3V4h1c0.27 0.02 0.48 0.11 0.69 0.31s0.3 0.42 0.31 0.69v6.28c-0.59 0.34-1 0.98-1 1.72 0 1.11 0.89 2 2 2s2-0.89 2-2c0-0.73-0.41-1.38-1-1.72z m-1 2.92c-0.66 0-1.2-0.55-1.2-1.2s0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2-0.55 1.2-1.2 1.2zM4 3c0-1.11-0.89-2-2-2S0 1.89 0 3c0 0.73 0.41 1.38 1 1.72 0 1.55 0 5.56 0 6.56-0.59 0.34-1 0.98-1 1.72 0 1.11 0.89 2 2 2s2-0.89 2-2c0-0.73-0.41-1.38-1-1.72V4.72c0.59-0.34 1-0.98 1-1.72z m-0.8 10c0 0.66-0.55 1.2-1.2 1.2s-1.2-0.55-1.2-1.2 0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2z m-1.2-8.8c-0.66 0-1.2-0.55-1.2-1.2s0.55-1.2 1.2-1.2 1.2 0.55 1.2 1.2-0.55 1.2-1.2 1.2z"></path></svg>
      <span itemprop="name">Pull requests</span>
      <span class="counter">0</span>
      <meta itemprop="position" content="3">
</a>  </span>



  <a href="/litehelpers/Cordova-sqlite-storage/pulse" class="js-selected-navigation-item reponav-item" data-selected-links="pulse /litehelpers/Cordova-sqlite-storage/pulse">
    <svg aria-hidden="true" class="octicon octicon-pulse" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M11.5 8L8.8 5.4 6.6 8.5 5.5 1.6 2.38 8H0V10h3.6L4.5 8.2l0.9 5.4L9 8.5l1.6 1.5H14V8H11.5z"></path></svg>
    Pulse
</a>
  <a href="/litehelpers/Cordova-sqlite-storage/graphs" class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors /litehelpers/Cordova-sqlite-storage/graphs">
    <svg aria-hidden="true" class="octicon octicon-graph" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M16 14v1H0V0h1v14h15z m-11-1H3V8h2v5z m4 0H7V3h2v10z m4 0H11V6h2v7z"></path></svg>
    Graphs
</a>

</nav>

  </div>
</div>

<div class="container new-discussion-timeline experiment-repo-nav">
  <div class="repository-content">

    

<a href="/litehelpers/Cordova-sqlite-storage/blob/c887995ac23a2f3b2ee84e2b49b0a233a6e3a183/SQLitePlugin.coffee.md" class="hidden js-permalink-shortcut" data-hotkey="y">Permalink</a>

<!-- blob contrib key: blob_contributors:v21:83ebdc2768c4cf44beb6495b05ba646b -->

<div class="file-navigation js-zeroclipboard-container">
  
<div class="select-menu branch-select-menu js-menu-container js-select-menu left">
  <button class="btn btn-sm select-menu-button js-menu-target css-truncate" data-hotkey="w"
    title="storage-master"
    type="button" aria-label="Switch branches or tags" tabindex="0" aria-haspopup="true">
    <i>Branch:</i>
    <span class="js-select-button css-truncate-target">storage-master</span>
  </button>

  <div class="select-menu-modal-holder js-menu-content js-navigation-container" data-pjax aria-hidden="true">

    <div class="select-menu-modal">
      <div class="select-menu-header">
        <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48-3.75-3.75-3.75 3.75-1.48-1.48 3.75-3.75L0.77 4.25l1.48-1.48 3.75 3.75 3.75-3.75 1.48 1.48-3.75 3.75z"></path></svg>
        <span class="select-menu-title">Switch branches/tags</span>
      </div>

      <div class="select-menu-filters">
        <div class="select-menu-text-filter">
          <input type="text" aria-label="Filter branches/tags" id="context-commitish-filter-field" class="form-control js-filterable-field js-navigation-enable" placeholder="Filter branches/tags">
        </div>
        <div class="select-menu-tabs">
          <ul>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="branches" data-filter-placeholder="Filter branches/tags" class="js-select-menu-tab" role="tab">Branches</a>
            </li>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="tags" data-filter-placeholder="Find a tag…" class="js-select-menu-tab" role="tab">Tags</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="branches" role="menu">

        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/cb-Diliz-add-closedb-externalstorage-2/SQLitePlugin.coffee.md"
               data-name="cb-Diliz-add-closedb-externalstorage-2"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="cb-Diliz-add-closedb-externalstorage-2">
                cb-Diliz-add-closedb-externalstorage-2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/common-src/SQLitePlugin.coffee.md"
               data-name="common-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="common-src">
                common-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/common-test/SQLitePlugin.coffee.md"
               data-name="common-test"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="common-test">
                common-test
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/cordova-sqlite-common/SQLitePlugin.coffee.md"
               data-name="cordova-sqlite-common"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="cordova-sqlite-common">
                cordova-sqlite-common
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/cordova-sqlite-test/SQLitePlugin.coffee.md"
               data-name="cordova-sqlite-test"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="cordova-sqlite-test">
                cordova-sqlite-test
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/master-rc/SQLitePlugin.coffee.md"
               data-name="master-rc"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="master-rc">
                master-rc
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/master-src/SQLitePlugin.coffee.md"
               data-name="master-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="master-src">
                master-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/new-common-rc/SQLitePlugin.coffee.md"
               data-name="new-common-rc"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="new-common-rc">
                new-common-rc
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/new-common-src/SQLitePlugin.coffee.md"
               data-name="new-common-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="new-common-src">
                new-common-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/new-src/SQLitePlugin.coffee.md"
               data-name="new-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="new-src">
                new-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open selected"
               href="/litehelpers/Cordova-sqlite-storage/blob/storage-master/SQLitePlugin.coffee.md"
               data-name="storage-master"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="storage-master">
                storage-master
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/vb-master-dev-with-wp-dll-2014.07/SQLitePlugin.coffee.md"
               data-name="vb-master-dev-with-wp-dll-2014.07"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="vb-master-dev-with-wp-dll-2014.07">
                vb-master-dev-with-wp-dll-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/windows-common-src/SQLitePlugin.coffee.md"
               data-name="windows-common-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="windows-common-src">
                windows-common-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/windows-common/SQLitePlugin.coffee.md"
               data-name="windows-common"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="windows-common">
                windows-common
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/wp-master-rc/SQLitePlugin.coffee.md"
               data-name="wp-master-rc"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="wp-master-rc">
                wp-master-rc
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/wp-src/SQLitePlugin.coffee.md"
               data-name="wp-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="wp-src">
                wp-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-Diliz-add-closedb-externalstorage-1/SQLitePlugin.coffee.md"
               data-name="xb-Diliz-add-closedb-externalstorage-1"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-Diliz-add-closedb-externalstorage-1">
                xb-Diliz-add-closedb-externalstorage-1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-aarononeal-201501/SQLitePlugin.coffee.md"
               data-name="xb-aarononeal-201501"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-aarononeal-201501">
                xb-aarononeal-201501
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-aarononeal-201502/SQLitePlugin.coffee.md"
               data-name="xb-aarononeal-201502"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-aarononeal-201502">
                xb-aarononeal-201502
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-android-json-error-code-2013.08/SQLitePlugin.coffee.md"
               data-name="xb-android-json-error-code-2013.08"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-android-json-error-code-2013.08">
                xb-android-json-error-code-2013.08
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-android-lock-workaround/SQLitePlugin.coffee.md"
               data-name="xb-android-lock-workaround"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-android-lock-workaround">
                xb-android-lock-workaround
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-first-sqlite4java-amd64-fix/SQLitePlugin.coffee.md"
               data-name="xb-first-sqlite4java-amd64-fix"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-first-sqlite4java-amd64-fix">
                xb-first-sqlite4java-amd64-fix
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-full-test-rc/SQLitePlugin.coffee.md"
               data-name="xb-full-test-rc"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-full-test-rc">
                xb-full-test-rc
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-ios-ef4-tx-fix-in-coffeescript-2013.07/SQLitePlugin.coffee.md"
               data-name="xb-ios-ef4-tx-fix-in-coffeescript-2013.07"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-ios-ef4-tx-fix-in-coffeescript-2013.07">
                xb-ios-ef4-tx-fix-in-coffeescript-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-mark-wp8-callbacks/SQLitePlugin.coffee.md"
               data-name="xb-mark-wp8-callbacks"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-mark-wp8-callbacks">
                xb-mark-wp8-callbacks
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-new-rc-20150330/SQLitePlugin.coffee.md"
               data-name="xb-new-rc-20150330"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-new-rc-20150330">
                xb-new-rc-20150330
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-old-common-src/SQLitePlugin.coffee.md"
               data-name="xb-old-common-src"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-old-common-src">
                xb-old-common-src
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-open-cb-fix/SQLitePlugin.coffee.md"
               data-name="xb-open-cb-fix"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-open-cb-fix">
                xb-open-cb-fix
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-rikshadriver-2013-10/SQLitePlugin.coffee.md"
               data-name="xb-rikshadriver-2013-10"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-rikshadriver-2013-10">
                xb-rikshadriver-2013-10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-rikshadriver-2014-03/SQLitePlugin.coffee.md"
               data-name="xb-rikshadriver-2014-03"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-rikshadriver-2014-03">
                xb-rikshadriver-2014-03
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-sqlite4java-test1/SQLitePlugin.coffee.md"
               data-name="xb-sqlite4java-test1"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-sqlite4java-test1">
                xb-sqlite4java-test1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-vacation-2014-09/SQLitePlugin.coffee.md"
               data-name="xb-vacation-2014-09"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-vacation-2014-09">
                xb-vacation-2014-09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-vldmrrr-windows-pr1/SQLitePlugin.coffee.md"
               data-name="xb-vldmrrr-windows-pr1"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-vldmrrr-windows-pr1">
                xb-vldmrrr-windows-pr1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-vldmrrr-windows-pr2/SQLitePlugin.coffee.md"
               data-name="xb-vldmrrr-windows-pr2"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-vldmrrr-windows-pr2">
                xb-vldmrrr-windows-pr2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-welldone-software-ios-lock-fix-1/SQLitePlugin.coffee.md"
               data-name="xb-welldone-software-ios-lock-fix-1"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-welldone-software-ios-lock-fix-1">
                xb-welldone-software-ios-lock-fix-1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-windows-test-2015-03/SQLitePlugin.coffee.md"
               data-name="xb-windows-test-2015-03"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-windows-test-2015-03">
                xb-windows-test-2015-03
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-wp-csharp-sqlite-2013.10/SQLitePlugin.coffee.md"
               data-name="xb-wp-csharp-sqlite-2013.10"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-wp-csharp-sqlite-2013.10">
                xb-wp-csharp-sqlite-2013.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/litehelpers/Cordova-sqlite-storage/blob/xb-wp8-native-2013.09/SQLitePlugin.coffee.md"
               data-name="xb-wp8-native-2013.09"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text" title="xb-wp8-native-2013.09">
                xb-wp8-native-2013.09
              </span>
            </a>
        </div>

          <div class="select-menu-no-results">Nothing to show</div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="tags">
        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/xv-wp8-dllimport-pre-merge-2014.07/SQLitePlugin.coffee.md"
              data-name="xv-wp8-dllimport-pre-merge-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="xv-wp8-dllimport-pre-merge-2014.07">
                xv-wp8-dllimport-pre-merge-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/xv-wp8-dllimport-merge-2014.07/SQLitePlugin.coffee.md"
              data-name="xv-wp8-dllimport-merge-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="xv-wp8-dllimport-merge-2014.07">
                xv-wp8-dllimport-merge-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/xv-pre-wp8-merge-2014.07/SQLitePlugin.coffee.md"
              data-name="xv-pre-wp8-merge-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="xv-pre-wp8-merge-2014.07">
                xv-pre-wp8-merge-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/xt-open-cb-success-fix-android-2013.10/SQLitePlugin.coffee.md"
              data-name="xt-open-cb-success-fix-android-2013.10"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="xt-open-cb-success-fix-android-2013.10">
                xt-open-cb-success-fix-android-2013.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/xt-ios-ef4-tx-fix-in-coffeescript-2013.07/SQLitePlugin.coffee.md"
              data-name="xt-ios-ef4-tx-fix-in-coffeescript-2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="xt-ios-ef4-tx-fix-in-coffeescript-2013.07">
                xt-ios-ef4-tx-fix-in-coffeescript-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/wp-csharp-sqlite-pre-merge-2014-1/SQLitePlugin.coffee.md"
              data-name="wp-csharp-sqlite-pre-merge-2014-1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="wp-csharp-sqlite-pre-merge-2014-1">
                wp-csharp-sqlite-pre-merge-2014-1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/wp-csharp-sqlite-2014-2/SQLitePlugin.coffee.md"
              data-name="wp-csharp-sqlite-2014-2"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="wp-csharp-sqlite-2014-2">
                wp-csharp-sqlite-2014-2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/wp-csharp-sqlite-2014-1/SQLitePlugin.coffee.md"
              data-name="wp-csharp-sqlite-2014-1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="wp-csharp-sqlite-2014-1">
                wp-csharp-sqlite-2014-1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-orig-2013.07/SQLitePlugin.coffee.md"
              data-name="vv-wp-orig-2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-orig-2013.07">
                vv-wp-orig-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-dlls-first-2014.07/SQLitePlugin.coffee.md"
              data-name="vv-wp-dlls-first-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-dlls-first-2014.07">
                vv-wp-dlls-first-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-csharp-sqlite-src-2013.09/SQLitePlugin.coffee.md"
              data-name="vv-wp-csharp-sqlite-src-2013.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-csharp-sqlite-src-2013.09">
                vv-wp-csharp-sqlite-src-2013.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-csharp-sqlite-pre-merge-1-2014.07/SQLitePlugin.coffee.md"
              data-name="vv-wp-csharp-sqlite-pre-merge-1-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-csharp-sqlite-pre-merge-1-2014.07">
                vv-wp-csharp-sqlite-pre-merge-1-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-csharp-sqlite-pre-2013.09/SQLitePlugin.coffee.md"
              data-name="vv-wp-csharp-sqlite-pre-2013.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-csharp-sqlite-pre-2013.09">
                vv-wp-csharp-sqlite-pre-2013.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-csharp-merge-2-2014.07/SQLitePlugin.coffee.md"
              data-name="vv-wp-csharp-merge-2-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-csharp-merge-2-2014.07">
                vv-wp-csharp-merge-2-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-wp-csharp-merge-1-2014.07/SQLitePlugin.coffee.md"
              data-name="vv-wp-csharp-merge-1-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-wp-csharp-merge-1-2014.07">
                vv-wp-csharp-merge-1-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-windows-arm-fix-2015.04.28/SQLitePlugin.coffee.md"
              data-name="vv-windows-arm-fix-2015.04.28"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-windows-arm-fix-2015.04.28">
                vv-windows-arm-fix-2015.04.28
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-perflogs-2013.09-0/SQLitePlugin.coffee.md"
              data-name="vv-perflogs-2013.09-0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-perflogs-2013.09-0">
                vv-perflogs-2013.09-0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-ios-pre-merge-2012.04/SQLitePlugin.coffee.md"
              data-name="vv-orig-ios-pre-merge-2012.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-ios-pre-merge-2012.04">
                vv-orig-ios-pre-merge-2012.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-ios-first-2011.06/SQLitePlugin.coffee.md"
              data-name="vv-orig-ios-first-2011.06"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-ios-first-2011.06">
                vv-orig-ios-first-2011.06
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-droidgap-2014.04/SQLitePlugin.coffee.md"
              data-name="vv-orig-droidgap-2014.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-droidgap-2014.04">
                vv-orig-droidgap-2014.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-android-pre-merge-2012.04/SQLitePlugin.coffee.md"
              data-name="vv-orig-android-pre-merge-2012.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-android-pre-merge-2012.04">
                vv-orig-android-pre-merge-2012.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-android-ios-combo-merge-2014.04/SQLitePlugin.coffee.md"
              data-name="vv-orig-android-ios-combo-merge-2014.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-android-ios-combo-merge-2014.04">
                vv-orig-android-ios-combo-merge-2014.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-orig-android-ios-combo-2012.12/SQLitePlugin.coffee.md"
              data-name="vv-orig-android-ios-combo-2012.12"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-orig-android-ios-combo-2012.12">
                vv-orig-android-ios-combo-2012.12
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-stormtek-2013.06/SQLitePlugin.coffee.md"
              data-name="vv-ios-stormtek-2013.06"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-stormtek-2013.06">
                vv-ios-stormtek-2013.06
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-r2013.08/SQLitePlugin.coffee.md"
              data-name="vv-ios-r2013.08"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-r2013.08">
                vv-ios-r2013.08
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-r2013.07/SQLitePlugin.coffee.md"
              data-name="vv-ios-r2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-r2013.07">
                vv-ios-r2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-r2013.05/SQLitePlugin.coffee.md"
              data-name="vv-ios-r2013.05"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-r2013.05">
                vv-ios-r2013.05
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-pre-merge-2013.09/SQLitePlugin.coffee.md"
              data-name="vv-ios-pre-merge-2013.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-pre-merge-2013.09">
                vv-ios-pre-merge-2013.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-json-error-fix-2013.08/SQLitePlugin.coffee.md"
              data-name="vv-ios-json-error-fix-2013.08"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-json-error-fix-2013.08">
                vv-ios-json-error-fix-2013.08
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-exec-json-fix-2013.08/SQLitePlugin.coffee.md"
              data-name="vv-ios-exec-json-fix-2013.08"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-exec-json-fix-2013.08">
                vv-ios-exec-json-fix-2013.08
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-ios-bind-number-values-as-numbers-2013.05/SQLitePlugin.coffee.md"
              data-name="vv-ios-bind-number-values-as-numbers-2013.05"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-ios-bind-number-values-as-numbers-2013.05">
                vv-ios-bind-number-values-as-numbers-2013.05
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-fix-cb-order-2014.07/SQLitePlugin.coffee.md"
              data-name="vv-fix-cb-order-2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-fix-cb-order-2014.07">
                vv-fix-cb-order-2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-droidgap-orig-2012.04/SQLitePlugin.coffee.md"
              data-name="vv-droidgap-orig-2012.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-droidgap-orig-2012.04">
                vv-droidgap-orig-2012.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-tx-cb-fix-2013.07/SQLitePlugin.coffee.md"
              data-name="vv-android-tx-cb-fix-2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-tx-cb-fix-2013.07">
                vv-android-tx-cb-fix-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-pre-merge-2013.09/SQLitePlugin.coffee.md"
              data-name="vv-android-pre-merge-2013.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-pre-merge-2013.09">
                vv-android-pre-merge-2013.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-orig-2012.04/SQLitePlugin.coffee.md"
              data-name="vv-android-orig-2012.04"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-orig-2012.04">
                vv-android-orig-2012.04
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-ios-merge-2013.09/SQLitePlugin.coffee.md"
              data-name="vv-android-ios-merge-2013.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-ios-merge-2013.09">
                vv-android-ios-merge-2013.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-ics-tx-fix-2013.10/SQLitePlugin.coffee.md"
              data-name="vv-android-ics-tx-fix-2013.10"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-ics-tx-fix-2013.10">
                vv-android-ics-tx-fix-2013.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-ef4-tx-fix-2013.07/SQLitePlugin.coffee.md"
              data-name="vv-android-ef4-tx-fix-2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-ef4-tx-fix-2013.07">
                vv-android-ef4-tx-fix-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-ef4-tx-error-fix-2013.07/SQLitePlugin.coffee.md"
              data-name="vv-android-ef4-tx-error-fix-2013.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-ef4-tx-error-fix-2013.07">
                vv-android-ef4-tx-error-fix-2013.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-2013.02/SQLitePlugin.coffee.md"
              data-name="vv-android-2013.02"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-2013.02">
                vv-android-2013.02
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-android-2013.01/SQLitePlugin.coffee.md"
              data-name="vv-android-2013.01"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-android-2013.01">
                vv-android-2013.01
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/vv-2013.09-perflogs-1/SQLitePlugin.coffee.md"
              data-name="vv-2013.09-perflogs-1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="vv-2013.09-perflogs-1">
                vv-2013.09-perflogs-1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2015.02/SQLitePlugin.coffee.md"
              data-name="r2015.02"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2015.02">
                r2015.02
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2014.09/SQLitePlugin.coffee.md"
              data-name="r2014.09"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2014.09">
                r2014.09
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2014.07/SQLitePlugin.coffee.md"
              data-name="r2014.07"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2014.07">
                r2014.07
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2014.06/SQLitePlugin.coffee.md"
              data-name="r2014.06"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2014.06">
                r2014.06
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2013.10/SQLitePlugin.coffee.md"
              data-name="r2013.10"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2013.10">
                r2013.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2013.05/SQLitePlugin.coffee.md"
              data-name="r2013.05"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2013.05">
                r2013.05
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2012.11/SQLitePlugin.coffee.md"
              data-name="r2012.11"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2012.11">
                r2012.11
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r2012.10/SQLitePlugin.coffee.md"
              data-name="r2012.10"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r2012.10">
                r2012.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r1.0.4/SQLitePlugin.coffee.md"
              data-name="r1.0.4"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r1.0.4">
                r1.0.4
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/r0.7.5-old/SQLitePlugin.coffee.md"
              data-name="r0.7.5-old"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="r0.7.5-old">
                r0.7.5-old
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/1.4.1/SQLitePlugin.coffee.md"
              data-name="1.4.1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="1.4.1">
                1.4.1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/1.4.0/SQLitePlugin.coffee.md"
              data-name="1.4.0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="1.4.0">
                1.4.0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/1.2.2/SQLitePlugin.coffee.md"
              data-name="1.2.2"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="1.2.2">
                1.2.2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/1.2.1/SQLitePlugin.coffee.md"
              data-name="1.2.1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="1.2.1">
                1.2.1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/1.2.0/SQLitePlugin.coffee.md"
              data-name="1.2.0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="1.2.0">
                1.2.0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.8.5/SQLitePlugin.coffee.md"
              data-name="0.8.5"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.8.5">
                0.8.5
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.8.2/SQLitePlugin.coffee.md"
              data-name="0.8.2"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.8.2">
                0.8.2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.14/SQLitePlugin.coffee.md"
              data-name="0.7.14"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.14">
                0.7.14
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.13/SQLitePlugin.coffee.md"
              data-name="0.7.13"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.13">
                0.7.13
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.12/SQLitePlugin.coffee.md"
              data-name="0.7.12"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.12">
                0.7.12
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.11/SQLitePlugin.coffee.md"
              data-name="0.7.11"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.11">
                0.7.11
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.10/SQLitePlugin.coffee.md"
              data-name="0.7.10"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.10">
                0.7.10
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.9/SQLitePlugin.coffee.md"
              data-name="0.7.9"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.9">
                0.7.9
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.8/SQLitePlugin.coffee.md"
              data-name="0.7.8"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.8">
                0.7.8
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.7/SQLitePlugin.coffee.md"
              data-name="0.7.7"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.7">
                0.7.7
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.6/SQLitePlugin.coffee.md"
              data-name="0.7.6"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.6">
                0.7.6
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/litehelpers/Cordova-sqlite-storage/tree/0.7.5/SQLitePlugin.coffee.md"
              data-name="0.7.5"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5L4 13 0 9l1.5-1.5 2.5 2.5 6.5-6.5 1.5 1.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.7.5">
                0.7.5
              </span>
            </a>
        </div>

        <div class="select-menu-no-results">Nothing to show</div>
      </div>

    </div>
  </div>
</div>

  <div class="btn-group right">
    <a href="/litehelpers/Cordova-sqlite-storage/find/storage-master"
          class="js-pjax-capture-input btn btn-sm"
          data-pjax
          data-hotkey="t">
      Find file
    </a>
    <button aria-label="Copy file path to clipboard" class="js-zeroclipboard btn btn-sm zeroclipboard-button tooltipped tooltipped-s" data-copied-hint="Copied!" type="button">Copy path</button>
  </div>
  <div class="breadcrumb js-zeroclipboard-target">
    <span class="repo-root js-repo-root"><span class="js-path-segment"><a href="/litehelpers/Cordova-sqlite-storage"><span>Cordova-sqlite-storage</span></a></span></span><span class="separator">/</span><strong class="final-path">SQLitePlugin.coffee.md</strong>
  </div>
</div>


  <div class="commit-tease">
      <span class="right">
        <a class="commit-tease-sha" href="/litehelpers/Cordova-sqlite-storage/commit/5ef812444d72a4e223c09a0975c5586e23d8d209" data-pjax>
          5ef8124
        </a>
        <relative-time datetime="2016-04-26T09:08:32Z">Apr 26, 2016</relative-time>
      </span>
      <div>
        <img alt="@brodybits" class="avatar" height="20" src="https://avatars3.githubusercontent.com/u/1559888?v=3&amp;s=40" width="20" />
        <a href="/brodybits" class="user-mention" rel="contributor">brodybits</a>
          <a href="/litehelpers/Cordova-sqlite-storage/commit/5ef812444d72a4e223c09a0975c5586e23d8d209" class="message" data-pjax="true" title="Self-test function to verify ability to open/populate/read/delete a test database">Self-test function to verify ability to open/populate/read/delete a t…</a>
      </div>

    <div class="commit-tease-contributors">
      <button type="button" class="btn-link muted-link contributors-toggle" data-facebox="#blob_contributors_box">
        <strong>3</strong>
         contributors
      </button>
          <a class="avatar-link tooltipped tooltipped-s" aria-label="brodybits" href="/litehelpers/Cordova-sqlite-storage/commits/storage-master/SQLitePlugin.coffee.md?author=brodybits"><img alt="@brodybits" class="avatar" height="20" src="https://avatars3.githubusercontent.com/u/1559888?v=3&amp;s=40" width="20" /> </a>
    <a class="avatar-link tooltipped tooltipped-s" aria-label="aarononeal" href="/litehelpers/Cordova-sqlite-storage/commits/storage-master/SQLitePlugin.coffee.md?author=aarononeal"><img alt="@aarononeal" class="avatar" height="20" src="https://avatars1.githubusercontent.com/u/1740567?v=3&amp;s=40" width="20" /> </a>
    <a class="avatar-link tooltipped tooltipped-s" aria-label="nolanlawson" href="/litehelpers/Cordova-sqlite-storage/commits/storage-master/SQLitePlugin.coffee.md?author=nolanlawson"><img alt="@nolanlawson" class="avatar" height="20" src="https://avatars0.githubusercontent.com/u/283842?v=3&amp;s=40" width="20" /> </a>


    </div>

    <div id="blob_contributors_box" style="display:none">
      <h2 class="facebox-header" data-facebox-id="facebox-header">Users who have contributed to this file</h2>
      <ul class="facebox-user-list" data-facebox-id="facebox-description">
          <li class="facebox-user-list-item">
            <img alt="@brodybits" height="24" src="https://avatars1.githubusercontent.com/u/1559888?v=3&amp;s=48" width="24" />
            <a href="/brodybits">brodybits</a>
          </li>
          <li class="facebox-user-list-item">
            <img alt="@aarononeal" height="24" src="https://avatars3.githubusercontent.com/u/1740567?v=3&amp;s=48" width="24" />
            <a href="/aarononeal">aarononeal</a>
          </li>
          <li class="facebox-user-list-item">
            <img alt="@nolanlawson" height="24" src="https://avatars2.githubusercontent.com/u/283842?v=3&amp;s=48" width="24" />
            <a href="/nolanlawson">nolanlawson</a>
          </li>
      </ul>
    </div>
  </div>

<div class="file">
  <div class="file-header">
  <div class="file-actions">

    <div class="btn-group">
      <a href="/litehelpers/Cordova-sqlite-storage/raw/storage-master/SQLitePlugin.coffee.md" class="btn btn-sm " id="raw-url">Raw</a>
        <a href="/litehelpers/Cordova-sqlite-storage/blame/storage-master/SQLitePlugin.coffee.md" class="btn btn-sm js-update-url-with-hash">Blame</a>
      <a href="/litehelpers/Cordova-sqlite-storage/commits/storage-master/SQLitePlugin.coffee.md" class="btn btn-sm " rel="nofollow">History</a>
    </div>

        <a class="btn-octicon tooltipped tooltipped-nw"
           href="https://windows.github.com"
           aria-label="Open this file in GitHub Desktop"
           data-ga-click="Repository, open with desktop, type:windows">
            <svg aria-hidden="true" class="octicon octicon-device-desktop" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M15 2H1c-0.55 0-1 0.45-1 1v9c0 0.55 0.45 1 1 1h5.34c-0.25 0.61-0.86 1.39-2.34 2h8c-1.48-0.61-2.09-1.39-2.34-2h5.34c0.55 0 1-0.45 1-1V3c0-0.55-0.45-1-1-1z m0 9H1V3h14v8z"></path></svg>
        </a>

        <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/edit/storage-master/SQLitePlugin.coffee.md" class="inline-form js-update-url-with-hash" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="/15aWlLM/d6HIj38eYpAVd9yFfwtYzkCRYWd236BNSe1PGSNWVFzsqee2e3JUmMRqpB3LL4S/v2cEUzU4QdpjA==" /></div>
          <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
            aria-label="Fork this project and edit the file" data-hotkey="e" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-pencil" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M0 12v3h3l8-8-3-3L0 12z m3 2H1V12h1v1h1v1z m10.3-9.3l-1.3 1.3-3-3 1.3-1.3c0.39-0.39 1.02-0.39 1.41 0l1.59 1.59c0.39 0.39 0.39 1.02 0 1.41z"></path></svg>
          </button>
</form>        <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/litehelpers/Cordova-sqlite-storage/delete/storage-master/SQLitePlugin.coffee.md" class="inline-form" data-form-nonce="edfd2af0cb4d77a4c099a8afeeca6c4ddfdbf80b" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="VQFBobFBC6Bq/1AAR9PMo5ajkRcKBmA643NIWOlo37qGrMY1BASl1HDMcDZ/T7voe8ejslCbJXegAfu6AH0mGg==" /></div>
          <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
            aria-label="Fork this project and delete the file" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-trashcan" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M10 2H8c0-0.55-0.45-1-1-1H4c-0.55 0-1 0.45-1 1H1c-0.55 0-1 0.45-1 1v1c0 0.55 0.45 1 1 1v9c0 0.55 0.45 1 1 1h7c0.55 0 1-0.45 1-1V5c0.55 0 1-0.45 1-1v-1c0-0.55-0.45-1-1-1z m-1 12H2V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9z m1-10H1v-1h9v1z"></path></svg>
          </button>
</form>  </div>

  <div class="file-info">
      801 lines (607 sloc)
      <span class="file-info-divider"></span>
    26.2 KB
  </div>
</div>

  
  <div id="readme" class="readme blob instapaper_body">
    <article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-sqlite-plugin-in-markdown-litcoffee" class="anchor" href="#sqlite-plugin-in-markdown-litcoffee" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>SQLite plugin in Markdown (litcoffee)</h1>

<h4><a id="user-content-use-coffee-compiler-to-compile-this-directly-into-javascript" class="anchor" href="#use-coffee-compiler-to-compile-this-directly-into-javascript" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>Use coffee compiler to compile this directly into Javascript</h4>

<h4><a id="user-content-license-for-common-script-mit-or-apache" class="anchor" href="#license-for-common-script-mit-or-apache" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>License for common script: MIT or Apache</h4>

<h1><a id="user-content-top-level-sqlite-plugin-objects" class="anchor" href="#top-level-sqlite-plugin-objects" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>Top-level SQLite plugin objects</h1>

<h2><a id="user-content-root-window-object" class="anchor" href="#root-window-object" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>root window object:</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-v">root</span> <span class="pl-k">=</span> <span class="pl-smi">@</span></pre></div>

<h2><a id="user-content-constants" class="anchor" href="#constants" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>constant(s):</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-v">READ_ONLY_REGEX</span> <span class="pl-k">=</span> <span class="pl-sr"><span class="pl-pds">/</span><span class="pl-k">^</span><span class="pl-c1">\s</span><span class="pl-k">*</span>(?:drop<span class="pl-k">|</span>delete<span class="pl-k">|</span>insert<span class="pl-k">|</span>update<span class="pl-k">|</span>create)<span class="pl-c1">\s</span><span class="pl-pds">/</span>i</span>

<span class="pl-c"># per-db state</span>
<span class="pl-v">DB_STATE_INIT</span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>INIT<span class="pl-pds">"</span></span>
<span class="pl-v">DB_STATE_OPEN</span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>OPEN<span class="pl-pds">"</span></span></pre></div>

<h2><a id="user-content-globals" class="anchor" href="#globals" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>global(s):</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-c"># per-db map of locking and queueing</span>
<span class="pl-c"># XXX NOTE: This is NOT cleaned up when a db is closed and/or deleted.</span>
<span class="pl-c"># If the record is simply removed when a db is closed or deleted,</span>
<span class="pl-c"># it will cause some test failures and may break large-scale</span>
<span class="pl-c"># applications that repeatedly open and close the database.</span>
<span class="pl-c"># [BUG #210] TODO: better to abort and clean up the pending transaction state.</span>
<span class="pl-c"># XXX TBD this will be renamed and include some more per-db state.</span>
<span class="pl-v">txLocks</span> <span class="pl-k">=</span> {}</pre></div>

<h2><a id="user-content-utility-functions" class="anchor" href="#utility-functions" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>utility functions:</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-c"># Errors returned to callbacks must conform to `SqlError` with a code and message.</span>
<span class="pl-c"># Some errors are of type `Error` or `string` and must be converted.</span>
<span class="pl-en">newSQLError</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(error, code)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
  <span class="pl-v">sqlError</span> <span class="pl-k">=</span> error
  <span class="pl-v">code</span> <span class="pl-k">=</span> <span class="pl-c1">0</span> <span class="pl-k">if</span> <span class="pl-k">!</span>code <span class="pl-c"># unknown by default</span>

  <span class="pl-k">if</span> <span class="pl-k">!</span>sqlError
    <span class="pl-v">sqlError</span> <span class="pl-k">=</span> <span class="pl-k">new</span> <span class="pl-en">Error</span> <span class="pl-s"><span class="pl-pds">"</span>a plugin had an error but provided no response<span class="pl-pds">"</span></span>
    sqlError.<span class="pl-v">code</span> <span class="pl-k">=</span> code

  <span class="pl-k">if</span> <span class="pl-k">typeof</span> sqlError <span class="pl-k">is</span> <span class="pl-s"><span class="pl-pds">"</span>string<span class="pl-pds">"</span></span>
    <span class="pl-v">sqlError</span> <span class="pl-k">=</span> <span class="pl-k">new</span> <span class="pl-en">Error</span> error
    sqlError.<span class="pl-v">code</span> <span class="pl-k">=</span> code

  <span class="pl-k">if</span> <span class="pl-k">!</span>sqlError.code <span class="pl-k">&amp;&amp;</span> sqlError.message
    sqlError.<span class="pl-v">code</span> <span class="pl-k">=</span> code

  <span class="pl-k">if</span> <span class="pl-k">!</span>sqlError.code <span class="pl-k">&amp;&amp;</span> <span class="pl-k">!</span>sqlError.message
    <span class="pl-v">sqlError</span> <span class="pl-k">=</span> <span class="pl-k">new</span> <span class="pl-en">Error</span> <span class="pl-s"><span class="pl-pds">"</span>an unknown error was returned: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> JSON.<span class="pl-en">stringify</span>(sqlError)
    sqlError.<span class="pl-v">code</span> <span class="pl-k">=</span> code

  <span class="pl-k">return</span> sqlError

<span class="pl-v">nextTick</span> <span class="pl-k">=</span> <span class="pl-c1">window</span>.setImmediate <span class="pl-k">||</span> <span class="pl-smi">(fun)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c1">window</span>.<span class="pl-en">setTimeout</span>(fun, <span class="pl-c1">0</span>)
  <span class="pl-k">return</span>

<span class="pl-c">###</span>
<span class="pl-c">  Utility that avoids leaking the arguments object. See</span>
<span class="pl-c">  https://www.npmjs.org/package/argsarray</span>
<span class="pl-c">###</span>
<span class="pl-en">argsArray</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(fun)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
  <span class="pl-k">return</span> <span class="pl-k">-&gt;</span>
    <span class="pl-v">len</span> <span class="pl-k">=</span> arguments.length
    <span class="pl-k">if</span> len
      <span class="pl-v">args</span> <span class="pl-k">=</span> []
      <span class="pl-v">i</span> <span class="pl-k">=</span> <span class="pl-k">-</span><span class="pl-c1">1</span>
      <span class="pl-k">while</span> <span class="pl-k">++</span>i <span class="pl-k">&lt;</span> len
        args[i] <span class="pl-k">=</span> arguments[i]
      <span class="pl-k">return</span> fun.<span class="pl-en">call</span> <span class="pl-v">this</span>, args
    <span class="pl-k">else</span>
      <span class="pl-k">return</span> fun.<span class="pl-en">call</span> <span class="pl-v">this</span>, []</pre></div>

<h2><a id="user-content-sqlite-plugin-db-connection-handle" class="anchor" href="#sqlite-plugin-db-connection-handle" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>SQLite plugin db-connection handle</h2>

<h4><a id="user-content-note-there-can-be-multipe-sqliteplugin-db-connection-handles-per-open-db" class="anchor" href="#note-there-can-be-multipe-sqliteplugin-db-connection-handles-per-open-db" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>NOTE: there can be multipe SQLitePlugin db-connection handles per open db.</h4>

<h4><a id="user-content-sqlite-plugin-db-connection-handle-object-is-defined-by-a-constructor-function-and-prototype-member-functions" class="anchor" href="#sqlite-plugin-db-connection-handle-object-is-defined-by-a-constructor-function-and-prototype-member-functions" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>SQLite plugin db connection handle object is defined by a constructor function and prototype member functions:</h4>

<div class="highlight highlight-source-coffee"><pre><span class="pl-en">SQLitePlugin</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(openargs, openSuccess, openError)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
  <span class="pl-c"># console.log "SQLitePlugin openargs: #{JSON.stringify openargs}"</span>

  <span class="pl-c"># _should_ already be checked by openDatabase:</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span>(openargs <span class="pl-k">and</span> openargs[<span class="pl-s"><span class="pl-pds">'</span>name<span class="pl-pds">'</span></span>])
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>Cannot create a SQLitePlugin db instance without a db name<span class="pl-pds">"</span></span>

  <span class="pl-v">dbname</span> <span class="pl-k">=</span> openargs.name

  <span class="pl-k">if</span> <span class="pl-k">typeof</span> dbname <span class="pl-k">!=</span> <span class="pl-s"><span class="pl-pds">'</span>string<span class="pl-pds">'</span></span>
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>sqlite plugin database name must be a string<span class="pl-pds">'</span></span>

  <span class="pl-smi">@openargs</span> <span class="pl-k">=</span> openargs
  <span class="pl-smi">@dbname</span> <span class="pl-k">=</span> dbname

  <span class="pl-smi">@openSuccess</span> <span class="pl-k">=</span> openSuccess
  <span class="pl-smi">@openError</span> <span class="pl-k">=</span> openError

  <span class="pl-smi">@openSuccess</span> <span class="pl-k">or</span>
    @<span class="pl-en">openSuccess</span> <span class="pl-k">=</span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">"</span>DB opened: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> dbname
      <span class="pl-k">return</span>

  <span class="pl-smi">@openError</span> <span class="pl-k">or</span>
    @<span class="pl-en">openError</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(e)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> e.message
      <span class="pl-k">return</span>

  @<span class="pl-en">open</span> <span class="pl-smi">@openSuccess</span>, <span class="pl-smi">@openError</span>
  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span><span class="pl-v">databaseFeatures</span> <span class="pl-k">=</span> <span class="pl-v">isSQLitePluginDatabase</span>: <span class="pl-c1">true</span>

<span class="pl-c"># Keep track of state of open db connections</span>
<span class="pl-c"># XXX TBD this will be moved and renamed or</span>
<span class="pl-c"># combined with txLocks.</span>
SQLitePlugin<span class="pl-k">::</span><span class="pl-v">openDBs</span> <span class="pl-k">=</span> {}

SQLitePlugin<span class="pl-k">::</span>addTransaction <span class="pl-k">=</span> <span class="pl-smi">(t)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span>txLocks[<span class="pl-smi">@dbname</span>]
    txLocks[<span class="pl-smi">@dbname</span>] <span class="pl-k">=</span> {
      <span class="pl-v">queue</span>: []
      <span class="pl-v">inProgress</span>: <span class="pl-c1">false</span>
    }
  txLocks[<span class="pl-smi">@dbname</span>].queue.<span class="pl-en">push</span> t
  <span class="pl-k">if</span> <span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span> <span class="pl-k">&amp;&amp;</span> <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>] <span class="pl-k">isnt</span> DB_STATE_INIT
    <span class="pl-c"># XXX TODO: only when queue has length of 1 [and test it!!]</span>
    @<span class="pl-en">startNextTransaction</span>()

  <span class="pl-k">else</span>
    <span class="pl-k">if</span> <span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>new transaction is waiting for open operation<span class="pl-pds">'</span></span>
    <span class="pl-k">else</span>
      <span class="pl-c"># XXX TBD TODO: in this case (which should not happen), should abort and discard the transaction.</span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>database is closed, new transaction is [stuck] waiting until db is opened again!<span class="pl-pds">'</span></span>
  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>transaction <span class="pl-k">=</span> <span class="pl-smi">(fn, error, success)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c"># FUTURE TBD check for valid fn here</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span><span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>]
    <span class="pl-en">error</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>database not open<span class="pl-pds">'</span></span>
    <span class="pl-k">return</span>

  @<span class="pl-en">addTransaction</span> <span class="pl-k">new</span> <span class="pl-en">SQLitePluginTransaction</span>(<span class="pl-v">this</span>, fn, error, success, <span class="pl-c1">true</span>, <span class="pl-c1">false</span>)
  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>readTransaction <span class="pl-k">=</span> <span class="pl-smi">(fn, error, success)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c"># FUTURE TBD check for valid fn here (and add test for this)</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span><span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>]
    <span class="pl-en">error</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>database not open<span class="pl-pds">'</span></span>
    <span class="pl-k">return</span>

  @<span class="pl-en">addTransaction</span> <span class="pl-k">new</span> <span class="pl-en">SQLitePluginTransaction</span>(<span class="pl-v">this</span>, fn, error, success, <span class="pl-c1">false</span>, <span class="pl-c1">true</span>)
  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>startNextTransaction <span class="pl-k">=</span> <span class="pl-k">-&gt;</span>
  <span class="pl-v">self</span> <span class="pl-k">=</span> <span class="pl-smi">@</span>

  nextTick <span class="pl-k">=&gt;</span>
    <span class="pl-k">if</span> <span class="pl-k">!</span>(<span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span>) <span class="pl-k">||</span> <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>] <span class="pl-k">isnt</span> DB_STATE_OPEN
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>cannot start next transaction: database not open<span class="pl-pds">'</span></span>
      <span class="pl-k">return</span>

    <span class="pl-v">txLock</span> <span class="pl-k">=</span> txLocks[self.dbname]
    <span class="pl-k">if</span> <span class="pl-k">!</span>txLock
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>cannot start next transaction: database connection is lost<span class="pl-pds">'</span></span>
      <span class="pl-c"># XXX TBD TODO (BUG #210/??): abort all pending transactions with error cb [and test!!]</span>
      <span class="pl-c"># @abortAllPendingTransactions()</span>
      <span class="pl-k">return</span>

    <span class="pl-k">else</span> <span class="pl-k">if</span> txLock.queue.length <span class="pl-k">&gt;</span> <span class="pl-c1">0</span> <span class="pl-k">&amp;&amp;</span> <span class="pl-k">!</span>txLock.inProgress
      <span class="pl-c"># start next transaction in q</span>
      txLock.<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">true</span>
      txLock.queue.<span class="pl-en">shift</span>().<span class="pl-en">start</span>()
    <span class="pl-k">return</span>

  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>abortAllPendingTransactions <span class="pl-k">=</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c"># extra debug info:</span>
  <span class="pl-c"># if txLocks[@dbname] then console.log 'abortAllPendingTransactions with transaction queue length: ' + txLocks[@dbname].queue.length</span>
  <span class="pl-c"># else console.log 'abortAllPendingTransactions with no transaction lock state'</span>

  <span class="pl-v">txLock</span> <span class="pl-k">=</span> txLocks[<span class="pl-smi">@dbname</span>]
  <span class="pl-k">if</span> <span class="pl-k">!!</span>txLock <span class="pl-k">&amp;&amp;</span> txLock.queue.length <span class="pl-k">&gt;</span> <span class="pl-c1">0</span>
    <span class="pl-c"># XXX TODO: what to do in case there is a (stray) transaction in progress?</span>
    <span class="pl-c">#console.log 'abortAllPendingTransactions - cleanup old transaction(s)'</span>
    <span class="pl-k">for</span> tx <span class="pl-k">in</span> txLock.queue
      tx.<span class="pl-en">abortFromQ</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Invalid database handle<span class="pl-pds">'</span></span>

    <span class="pl-c"># XXX TODO: consider cleaning up (delete) txLocks[@dbname] resource,</span>
    <span class="pl-c"># in case it is known there are no more pending transactions</span>
    txLock.<span class="pl-v">queue</span> <span class="pl-k">=</span> []
    txLock.<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>

  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>open <span class="pl-k">=</span> <span class="pl-smi">(success, error)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span>
    <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>database already open: <span class="pl-pds">'</span></span> <span class="pl-k">+</span> <span class="pl-smi">@dbname</span>

    <span class="pl-c"># for a re-open run the success cb async so that the openDatabase return value</span>
    <span class="pl-c"># can be used in the success handler as an alternative to the handler's</span>
    <span class="pl-c"># db argument</span>
    nextTick <span class="pl-k">=&gt;</span>
      success <span class="pl-smi">@</span>
      <span class="pl-k">return</span>

  <span class="pl-k">else</span>
    <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>OPEN database: <span class="pl-pds">'</span></span> <span class="pl-k">+</span> <span class="pl-smi">@dbname</span>

    <span class="pl-en">opensuccesscb</span> <span class="pl-k">=</span> <span class="pl-k"><span class="pl-k">=&gt;</span></span>
      <span class="pl-c"># NOTE: the db state is NOT stored (in @openDBs) if the db was closed or deleted.</span>
      <span class="pl-c"># console.log 'OPEN database: ' + @dbname + ' succeeded'</span>

      <span class="pl-c">#if !@openDBs[@dbname] then call open error cb, and abort pending tx if any</span>
      <span class="pl-k">if</span> <span class="pl-k">!</span><span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>]
        <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>database was closed during open operation<span class="pl-pds">'</span></span>
        <span class="pl-c"># XXX TODO [BUG #210] (and test!!):</span>
        <span class="pl-c"># if !!error then error newSQLError 'database closed during open operation'</span>
        <span class="pl-c"># @abortAllPendingTransactions()</span>

      <span class="pl-k">if</span> <span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span>
        <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>] <span class="pl-k">=</span> DB_STATE_OPEN

      <span class="pl-k">if</span> <span class="pl-k">!!</span>success <span class="pl-k">then</span> success <span class="pl-smi">@</span>

      <span class="pl-v">txLock</span> <span class="pl-k">=</span> txLocks[<span class="pl-smi">@dbname</span>]
      <span class="pl-k">if</span> <span class="pl-k">!!</span>txLock <span class="pl-k">&amp;&amp;</span> txLock.queue.length <span class="pl-k">&gt;</span> <span class="pl-c1">0</span> <span class="pl-k">&amp;&amp;</span> <span class="pl-k">!</span>txLock.inProgress
        @<span class="pl-en">startNextTransaction</span>()
      <span class="pl-k">return</span>

    <span class="pl-en">openerrorcb</span> <span class="pl-k">=</span> <span class="pl-k"><span class="pl-k">=&gt;</span></span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>OPEN database: <span class="pl-pds">'</span></span> <span class="pl-k">+</span> <span class="pl-smi">@dbname</span> <span class="pl-k">+</span> <span class="pl-s"><span class="pl-pds">'</span> failed, aborting any pending transactions<span class="pl-pds">'</span></span>
      <span class="pl-c"># XXX TODO: newSQLError missing the message part!</span>
      <span class="pl-k">if</span> <span class="pl-k">!!</span>error <span class="pl-k">then</span> <span class="pl-en">error</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Could not open database<span class="pl-pds">'</span></span>
      <span class="pl-k">delete</span> <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>]
      @<span class="pl-en">abortAllPendingTransactions</span>()
      <span class="pl-k">return</span>

    <span class="pl-c"># store initial DB state:</span>
    <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>] <span class="pl-k">=</span> DB_STATE_INIT

    cordova.<span class="pl-en">exec</span> opensuccesscb, openerrorcb, <span class="pl-s"><span class="pl-pds">"</span>SQLitePlugin<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>open<span class="pl-pds">"</span></span>, [ <span class="pl-smi">@openargs</span> ]

  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>close <span class="pl-k">=</span> <span class="pl-smi">(success, error)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-smi">@dbname</span> <span class="pl-k">of</span> <span class="pl-smi">@openDBs</span>
    <span class="pl-k">if</span> txLocks[<span class="pl-smi">@dbname</span>] <span class="pl-k">&amp;&amp;</span> txLocks[<span class="pl-smi">@dbname</span>].inProgress
      <span class="pl-c"># XXX TBD: wait for current tx then close (??)</span>
      <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>cannot close: transaction is in progress<span class="pl-pds">'</span></span>
      <span class="pl-en">error</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>database cannot be closed while a transaction is in progress<span class="pl-pds">'</span></span>
      <span class="pl-k">return</span>

    <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>CLOSE database: <span class="pl-pds">'</span></span> <span class="pl-k">+</span> <span class="pl-smi">@dbname</span>

    <span class="pl-c"># XXX [BUG #209] closing one db handle disables other handles to same db</span>
    <span class="pl-k">delete</span> <span class="pl-smi">@openDBs</span>[<span class="pl-smi">@dbname</span>]

    <span class="pl-k">if</span> txLocks[<span class="pl-smi">@dbname</span>] <span class="pl-k">then</span> <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>closing db with transaction queue length: <span class="pl-pds">'</span></span> <span class="pl-k">+</span> txLocks[<span class="pl-smi">@dbname</span>].queue.length
    <span class="pl-k">else</span> <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>closing db with no transaction lock state<span class="pl-pds">'</span></span>

    <span class="pl-c"># XXX [BUG #210] TODO: when closing or deleting a db, abort any pending transactions [and test it!!]</span>

    cordova.<span class="pl-en">exec</span> success, error, <span class="pl-s"><span class="pl-pds">"</span>SQLitePlugin<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>close<span class="pl-pds">"</span></span>, [ { <span class="pl-v">path</span>: <span class="pl-smi">@dbname</span> } ]

  <span class="pl-k">else</span>
    <span class="pl-en">console</span>.<span class="pl-en">log</span> <span class="pl-s"><span class="pl-pds">'</span>cannot close: database is not open<span class="pl-pds">'</span></span>
    <span class="pl-k">if</span> error <span class="pl-k">then</span> <span class="pl-en">nextTick</span> <span class="pl-k">-&gt;</span> <span class="pl-en">error</span>()

  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>executeSql <span class="pl-k">=</span> <span class="pl-smi">(statement, params, success, error)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c"># XXX TODO: better to capture the result, and report it once</span>
  <span class="pl-c"># the transaction has completely finished.</span>
  <span class="pl-c"># This would fix BUG #204 (cannot close db in db.executeSql() callback).</span>
  <span class="pl-en">mysuccess</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(t, r)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span> <span class="pl-k">if</span> <span class="pl-k">!!</span>success <span class="pl-k">then</span> <span class="pl-en">success</span> r
  <span class="pl-en">myerror</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(t, e)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span> <span class="pl-k">if</span> <span class="pl-k">!!</span>error <span class="pl-k">then</span> <span class="pl-en">error</span> e

  <span class="pl-en">myfn</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    tx.<span class="pl-en">addStatement</span>(statement, params, mysuccess, myerror)
    <span class="pl-k">return</span>

  @<span class="pl-en">addTransaction</span> <span class="pl-k">new</span> <span class="pl-en">SQLitePluginTransaction</span>(<span class="pl-v">this</span>, myfn, <span class="pl-c1">null</span>, <span class="pl-c1">null</span>, <span class="pl-c1">false</span>, <span class="pl-c1">false</span>)
  <span class="pl-k">return</span>

SQLitePlugin<span class="pl-k">::</span>sqlBatch <span class="pl-k">=</span> <span class="pl-smi">(sqlStatements, success, error)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span>sqlStatements <span class="pl-k">||</span> sqlStatements.constructor <span class="pl-k">isnt</span> <span class="pl-c1">Array</span>
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>sqlBatch expects an array<span class="pl-pds">'</span></span>

  <span class="pl-v">batchList</span> <span class="pl-k">=</span> []

  <span class="pl-k">for</span> st <span class="pl-k">in</span> sqlStatements
    <span class="pl-k">if</span> st.constructor <span class="pl-k">is</span> <span class="pl-c1">Array</span>
      <span class="pl-k">if</span> st.length <span class="pl-k">==</span> <span class="pl-c1">0</span>
        <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>sqlBatch array element of zero (0) length<span class="pl-pds">'</span></span>

      batchList.<span class="pl-c1">push</span>
        <span class="pl-v">sql</span>: st[<span class="pl-c1">0</span>]
        <span class="pl-v">params</span>: <span class="pl-k">if</span> st.length <span class="pl-k">==</span> <span class="pl-c1">0</span> <span class="pl-k">then</span> [] <span class="pl-k">else</span> st[<span class="pl-c1">1</span>]

    <span class="pl-k">else</span>
      batchList.<span class="pl-c1">push</span>
        <span class="pl-v">sql</span>: st
        <span class="pl-v">params</span>: []

  <span class="pl-en">myfn</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    <span class="pl-k">for</span> elem <span class="pl-k">in</span> batchList
      tx.<span class="pl-en">addStatement</span>(elem.sql, elem.params, <span class="pl-c1">null</span>, <span class="pl-c1">null</span>)

  @<span class="pl-en">addTransaction</span> <span class="pl-k">new</span> <span class="pl-en">SQLitePluginTransaction</span>(<span class="pl-v">this</span>, myfn, error, success, <span class="pl-c1">true</span>, <span class="pl-c1">false</span>)
  <span class="pl-k">return</span></pre></div>

<h2><a id="user-content-sqlite-plugin-transaction-object-for-batching" class="anchor" href="#sqlite-plugin-transaction-object-for-batching" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>SQLite plugin transaction object for batching:</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-en">SQLitePluginTransaction</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(db, fn, error, success, txlock, readOnly)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
  <span class="pl-c"># FUTURE TBD check this earlier:</span>
  <span class="pl-k">if</span> <span class="pl-k">typeof</span>(fn) <span class="pl-k">!=</span> <span class="pl-s"><span class="pl-pds">"</span>function<span class="pl-pds">"</span></span>
    <span class="pl-c">###</span>
<span class="pl-c">    This is consistent with the implementation in Chrome -- it</span>
<span class="pl-c">    throws if you pass anything other than a function. This also</span>
<span class="pl-c">    prevents us from stalling our txQueue if somebody passes a</span>
<span class="pl-c">    false value for fn.</span>
<span class="pl-c">    ###</span>
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>transaction expected a function<span class="pl-pds">"</span></span>

  <span class="pl-smi">@db</span> <span class="pl-k">=</span> db
  <span class="pl-smi">@fn</span> <span class="pl-k">=</span> fn
  <span class="pl-smi">@error</span> <span class="pl-k">=</span> error
  <span class="pl-smi">@success</span> <span class="pl-k">=</span> success
  <span class="pl-smi">@txlock</span> <span class="pl-k">=</span> txlock
  <span class="pl-smi">@readOnly</span> <span class="pl-k">=</span> readOnly
  <span class="pl-smi">@executes</span> <span class="pl-k">=</span> []

  <span class="pl-k">if</span> txlock
    @<span class="pl-en">addStatement</span> <span class="pl-s"><span class="pl-pds">"</span>BEGIN<span class="pl-pds">"</span></span>, [], <span class="pl-c1">null</span>, <span class="pl-smi">(tx, err)</span> <span class="pl-k">-&gt;</span>
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>unable to begin transaction: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> err.message, err.code

  <span class="pl-c"># Workaround for litehelpers/Cordova-sqlite-storage#409</span>
  <span class="pl-c"># extra statement in case user function does not add any SQL statements</span>
  <span class="pl-k">else</span>
    @<span class="pl-en">addStatement</span> <span class="pl-s"><span class="pl-pds">"</span>SELECT 1<span class="pl-pds">"</span></span>, [], <span class="pl-c1">null</span>, <span class="pl-c1">null</span>

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>start <span class="pl-k">=</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">try</span>
    @<span class="pl-en">fn</span> <span class="pl-v">this</span>
    @<span class="pl-en">run</span>()
  <span class="pl-k">catch</span> err
    <span class="pl-c"># If "fn" throws, we must report the whole transaction as failed.</span>
    txLocks[<span class="pl-smi">@db</span>.dbname].<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>
    <span class="pl-smi">@db</span>.<span class="pl-en">startNextTransaction</span>()
    <span class="pl-k">if</span> <span class="pl-smi">@error</span>
      @<span class="pl-en">error</span> <span class="pl-en">newSQLError</span> err
  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>executeSql <span class="pl-k">=</span> <span class="pl-smi">(sql, values, success, error)</span> <span class="pl-k">-&gt;</span>

  <span class="pl-k">if</span> <span class="pl-smi">@finalized</span>
    <span class="pl-k">throw</span> {<span class="pl-v">message</span>: <span class="pl-s"><span class="pl-pds">'</span>InvalidStateError: DOM Exception 11: This transaction is already finalized. Transactions are committed after its success or failure handlers are called. If you are using a Promise to handle callbacks, be aware that implementations following the A+ standard adhere to run-to-completion semantics and so Promise resolution occurs on a subsequent tick and therefore after the transaction commits.<span class="pl-pds">'</span></span>, <span class="pl-v">code</span>: <span class="pl-c1">11</span>}
    <span class="pl-k">return</span>

  <span class="pl-k">if</span> <span class="pl-smi">@readOnly</span> <span class="pl-k">&amp;&amp;</span> READ_ONLY_REGEX.<span class="pl-en">test</span>(sql)
    @<span class="pl-en">handleStatementFailure</span>(error, {<span class="pl-v">message</span>: <span class="pl-s"><span class="pl-pds">'</span>invalid sql for a read-only transaction<span class="pl-pds">'</span></span>})
    <span class="pl-k">return</span>

  @<span class="pl-en">addStatement</span>(sql, values, success, error)
  <span class="pl-k">return</span>

<span class="pl-c"># This method adds the SQL statement to the transaction queue but does not check for</span>
<span class="pl-c"># finalization since it is used to execute COMMIT and ROLLBACK.</span>
SQLitePluginTransaction<span class="pl-k">::</span>addStatement <span class="pl-k">=</span> <span class="pl-smi">(sql, values, success, error)</span> <span class="pl-k">-&gt;</span>

  <span class="pl-v">params</span> <span class="pl-k">=</span> []
  <span class="pl-k">if</span> <span class="pl-k">!!</span>values <span class="pl-k">&amp;&amp;</span> values.constructor <span class="pl-k">==</span> <span class="pl-c1">Array</span>
    <span class="pl-k">for</span> v <span class="pl-k">in</span> values
      <span class="pl-v">t</span> <span class="pl-k">=</span> <span class="pl-k">typeof</span> v
      params.<span class="pl-c1">push</span> (
        <span class="pl-k">if</span> v <span class="pl-k">==</span> <span class="pl-c1">null</span> <span class="pl-k">||</span> v <span class="pl-k">==</span> <span class="pl-c1">undefined</span> <span class="pl-k">||</span> t <span class="pl-k">==</span> <span class="pl-s"><span class="pl-pds">'</span>number<span class="pl-pds">'</span></span> <span class="pl-k">||</span> t <span class="pl-k">==</span> <span class="pl-s"><span class="pl-pds">'</span>string<span class="pl-pds">'</span></span> <span class="pl-k">then</span> v
        <span class="pl-k">else</span> <span class="pl-k">if</span> <span class="pl-en">v</span> <span class="pl-k">instanceof</span> <span class="pl-c1">Blob</span> <span class="pl-k">then</span> v.<span class="pl-en">valueOf</span>()
        <span class="pl-k">else</span> v.<span class="pl-en">toString</span>()
      )

  <span class="pl-smi">@executes</span>.<span class="pl-c1">push</span>
    <span class="pl-v">success</span>: success
    <span class="pl-v">error</span>: error

    <span class="pl-v">sql</span>: sql
    <span class="pl-v">params</span>: params

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>handleStatementSuccess <span class="pl-k">=</span> <span class="pl-smi">(handler, response)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span>handler
    <span class="pl-k">return</span>

  <span class="pl-v">rows</span> <span class="pl-k">=</span> response.rows <span class="pl-k">||</span> []
  <span class="pl-v">payload</span> <span class="pl-k">=</span>
    <span class="pl-v">rows</span>:
      <span class="pl-en">item</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(i)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
        rows[i]

      <span class="pl-v">length</span>: rows.length

    <span class="pl-v">rowsAffected</span>: response.rowsAffected <span class="pl-k">or</span> <span class="pl-c1">0</span>
    <span class="pl-v">insertId</span>: response.insertId <span class="pl-k">or</span> <span class="pl-c1">undefined</span>

  <span class="pl-en">handler</span> <span class="pl-v">this</span>, payload

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>handleStatementFailure <span class="pl-k">=</span> <span class="pl-smi">(handler, response)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-k">!</span>handler
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>a statement with no error handler failed: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> response.message, response.code
  <span class="pl-k">if</span> <span class="pl-en">handler</span>(<span class="pl-v">this</span>, response) <span class="pl-k">isnt</span> <span class="pl-c1">false</span>
    <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>a statement error callback did not return false: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> response.message, response.code
  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>run <span class="pl-k">=</span> <span class="pl-k">-&gt;</span>
  <span class="pl-v">txFailure</span> <span class="pl-k">=</span> <span class="pl-c1">null</span>

  <span class="pl-v">tropts</span> <span class="pl-k">=</span> []
  <span class="pl-v">batchExecutes</span> <span class="pl-k">=</span> <span class="pl-smi">@executes</span>
  <span class="pl-c"># NOTE: If this is zero it will not work. Workaround is applied in the constructor.</span>
  <span class="pl-c"># FUTURE TBD: It would be better to fix the problem here.</span>
  <span class="pl-v">waiting</span> <span class="pl-k">=</span> batchExecutes.length
  <span class="pl-smi">@executes</span> <span class="pl-k">=</span> []
  <span class="pl-v">tx</span> <span class="pl-k">=</span> <span class="pl-v">this</span>

  <span class="pl-en">handlerFor</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(index, didSucceed)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    <span class="pl-smi">(response)</span> <span class="pl-k">-&gt;</span>
      <span class="pl-k">try</span>
        <span class="pl-k">if</span> didSucceed
          tx.<span class="pl-en">handleStatementSuccess</span> batchExecutes[index].success, response
        <span class="pl-k">else</span>
          tx.<span class="pl-en">handleStatementFailure</span> batchExecutes[index].error, <span class="pl-en">newSQLError</span>(response)
      <span class="pl-k">catch</span> err
        <span class="pl-k">if</span> <span class="pl-k">!</span>txFailure
          <span class="pl-v">txFailure</span> <span class="pl-k">=</span> <span class="pl-en">newSQLError</span>(err)

      <span class="pl-k">if</span> <span class="pl-k">--</span>waiting <span class="pl-k">==</span> <span class="pl-c1">0</span>
        <span class="pl-k">if</span> txFailure
          tx.<span class="pl-en">abort</span> txFailure
        <span class="pl-k">else</span> <span class="pl-k">if</span> tx.executes.length <span class="pl-k">&gt;</span> <span class="pl-c1">0</span>
          <span class="pl-c"># new requests have been issued by the callback</span>
          <span class="pl-c"># handlers, so run another batch.</span>
          tx.<span class="pl-en">run</span>()
        <span class="pl-k">else</span>
          tx.<span class="pl-en">finish</span>()

      <span class="pl-k">return</span>

  <span class="pl-v">i</span> <span class="pl-k">=</span> <span class="pl-c1">0</span>

  <span class="pl-v">mycbmap</span> <span class="pl-k">=</span> {}

  <span class="pl-k">while</span> i <span class="pl-k">&lt;</span> batchExecutes.length
    <span class="pl-v">request</span> <span class="pl-k">=</span> batchExecutes[i]

    mycbmap[i] <span class="pl-k">=</span>
      <span class="pl-v">success</span>: <span class="pl-en">handlerFor</span>(i, <span class="pl-c1">true</span>)
      <span class="pl-v">error</span>: <span class="pl-en">handlerFor</span>(i, <span class="pl-c1">false</span>)

    tropts.<span class="pl-c1">push</span>
      <span class="pl-v">qid</span>: <span class="pl-c1">1111</span>
      <span class="pl-v">sql</span>: request.sql
      <span class="pl-v">params</span>: request.params

    i<span class="pl-k">++</span>

  <span class="pl-en">mycb</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(result)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    <span class="pl-c">#console.log "mycb result #{JSON.stringify result}"</span>

    <span class="pl-v">last</span> <span class="pl-k">=</span> result.length<span class="pl-k">-</span><span class="pl-c1">1</span>
    <span class="pl-k">for</span> i <span class="pl-k">in</span> [<span class="pl-c1">0</span><span class="pl-k">..</span>last]
      <span class="pl-v">r</span> <span class="pl-k">=</span> result[i]
      <span class="pl-v">type</span> <span class="pl-k">=</span> r.type
      <span class="pl-c"># NOTE: r.qid can be ignored</span>
      <span class="pl-v">res</span> <span class="pl-k">=</span> r.result

      <span class="pl-v">q</span> <span class="pl-k">=</span> mycbmap[i]

      <span class="pl-k">if</span> q
        <span class="pl-k">if</span> q[type]
          q[type] res

    <span class="pl-k">return</span>

  cordova.<span class="pl-en">exec</span> mycb, <span class="pl-c1">null</span>, <span class="pl-s"><span class="pl-pds">"</span>SQLitePlugin<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>backgroundExecuteSqlBatch<span class="pl-pds">"</span></span>, [{<span class="pl-v">dbargs</span>: {<span class="pl-v">dbname</span>: <span class="pl-smi">@db</span>.dbname}, <span class="pl-v">executes</span>: tropts}]

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>abort <span class="pl-k">=</span> <span class="pl-smi">(txFailure)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-smi">@finalized</span> <span class="pl-k">then</span> <span class="pl-k">return</span>
  <span class="pl-v">tx</span> <span class="pl-k">=</span> <span class="pl-smi">@</span>

  <span class="pl-en">succeeded</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    txLocks[tx.db.dbname].<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>
    tx.db.<span class="pl-en">startNextTransaction</span>()
    <span class="pl-k">if</span> tx.error <span class="pl-k">then</span> tx.<span class="pl-en">error</span> txFailure
    <span class="pl-k">return</span>

  <span class="pl-en">failed</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx, err)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    txLocks[tx.db.dbname].<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>
    tx.db.<span class="pl-en">startNextTransaction</span>()
    <span class="pl-k">if</span> tx.error <span class="pl-k">then</span> tx.<span class="pl-en">error</span> <span class="pl-en">newSQLError</span>(<span class="pl-s"><span class="pl-pds">"</span>error while trying to roll back: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> err.message, err.code)
    <span class="pl-k">return</span>

  <span class="pl-smi">@finalized</span> <span class="pl-k">=</span> <span class="pl-c1">true</span>

  <span class="pl-k">if</span> <span class="pl-smi">@txlock</span>
    @<span class="pl-en">addStatement</span> <span class="pl-s"><span class="pl-pds">"</span>ROLLBACK<span class="pl-pds">"</span></span>, [], succeeded, failed
    @<span class="pl-en">run</span>()
  <span class="pl-k">else</span>
    <span class="pl-en">succeeded</span>(tx)

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>finish <span class="pl-k">=</span> <span class="pl-k">-&gt;</span>
  <span class="pl-k">if</span> <span class="pl-smi">@finalized</span> <span class="pl-k">then</span> <span class="pl-k">return</span>
  <span class="pl-v">tx</span> <span class="pl-k">=</span> <span class="pl-smi">@</span>

  <span class="pl-en">succeeded</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    txLocks[tx.db.dbname].<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>
    tx.db.<span class="pl-en">startNextTransaction</span>()
    <span class="pl-k">if</span> tx.success <span class="pl-k">then</span> tx.<span class="pl-en">success</span>()
    <span class="pl-k">return</span>

  <span class="pl-en">failed</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(tx, err)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    txLocks[tx.db.dbname].<span class="pl-v">inProgress</span> <span class="pl-k">=</span> <span class="pl-c1">false</span>
    tx.db.<span class="pl-en">startNextTransaction</span>()
    <span class="pl-k">if</span> tx.error <span class="pl-k">then</span> tx.<span class="pl-en">error</span> <span class="pl-en">newSQLError</span>(<span class="pl-s"><span class="pl-pds">"</span>error while trying to commit: <span class="pl-pds">"</span></span> <span class="pl-k">+</span> err.message, err.code)
    <span class="pl-k">return</span>

  <span class="pl-smi">@finalized</span> <span class="pl-k">=</span> <span class="pl-c1">true</span>

  <span class="pl-k">if</span> <span class="pl-smi">@txlock</span>
    @<span class="pl-en">addStatement</span> <span class="pl-s"><span class="pl-pds">"</span>COMMIT<span class="pl-pds">"</span></span>, [], succeeded, failed
    @<span class="pl-en">run</span>()
  <span class="pl-k">else</span>
    <span class="pl-en">succeeded</span>(tx)

  <span class="pl-k">return</span>

SQLitePluginTransaction<span class="pl-k">::</span>abortFromQ <span class="pl-k">=</span> <span class="pl-smi">(sqlerror)</span> <span class="pl-k">-&gt;</span>
  <span class="pl-c"># NOTE: since the transaction is waiting in the queue,</span>
  <span class="pl-c"># the transaction function containing the SQL statements</span>
  <span class="pl-c"># would not be run yet. Simply report the transaction error.</span>
  <span class="pl-k">if</span> <span class="pl-smi">@error</span>
    @<span class="pl-en">error</span> sqlerror

  <span class="pl-k">return</span></pre></div>

<h2><a id="user-content-sqlite-plugin-object-factory" class="anchor" href="#sqlite-plugin-object-factory" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>SQLite plugin object factory:</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-c"># OLD:</span>
<span class="pl-v">dblocations</span> <span class="pl-k">=</span> [ <span class="pl-s"><span class="pl-pds">"</span>docs<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>libs<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>nosync<span class="pl-pds">"</span></span> ]

<span class="pl-v">iosLocationMap</span> <span class="pl-k">=</span>
  <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span> <span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>nosync<span class="pl-pds">'</span></span>
  <span class="pl-s"><span class="pl-pds">'</span>Documents<span class="pl-pds">'</span></span> <span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>docs<span class="pl-pds">'</span></span>
  <span class="pl-s"><span class="pl-pds">'</span>Library<span class="pl-pds">'</span></span> <span class="pl-k">:</span> <span class="pl-s"><span class="pl-pds">'</span>libs<span class="pl-pds">'</span></span>

<span class="pl-v">SQLiteFactory</span> <span class="pl-k">=</span>
  <span class="pl-c">###</span>
<span class="pl-c">  NOTE: this function should NOT be translated from Javascript</span>
<span class="pl-c">  back to CoffeeScript by js2coffee.</span>
<span class="pl-c">  If this function is edited in Javascript then someone will</span>
<span class="pl-c">  have to translate it back to CoffeeScript by hand.</span>
<span class="pl-c">  ###</span>
  <span class="pl-v">openDatabase</span>: argsArray <span class="pl-smi">(args)</span> <span class="pl-k">-&gt;</span>
    <span class="pl-k">if</span> args.length <span class="pl-k">&lt;</span> <span class="pl-c1">1</span> <span class="pl-k">||</span> <span class="pl-k">!</span>args[<span class="pl-c1">0</span>]
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Sorry missing mandatory open arguments object in openDatabase call<span class="pl-pds">'</span></span>

    <span class="pl-c">#first = args[0]</span>
    <span class="pl-c">#openargs = null</span>
    <span class="pl-c">#okcb = null</span>
    <span class="pl-c">#errorcb = null</span>

    <span class="pl-c">#if first.constructor == String</span>
    <span class="pl-c">#  openargs = {name: first}</span>

    <span class="pl-c">#  if args.length &gt;= 5</span>
    <span class="pl-c">#    okcb = args[4]</span>
    <span class="pl-c">#    if args.length &gt; 5 then errorcb = args[5]</span>

    <span class="pl-c">#else</span>
    <span class="pl-c">#  openargs = first</span>

    <span class="pl-c">#  if args.length &gt;= 2</span>
    <span class="pl-c">#    okcb = args[1]</span>
    <span class="pl-c">#    if args.length &gt; 2 then errorcb = args[2]</span>

    <span class="pl-k">if</span> args[<span class="pl-c1">0</span>].constructor <span class="pl-k">==</span> <span class="pl-c1">String</span>
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Sorry first openDatabase argument must be an object<span class="pl-pds">'</span></span>

    <span class="pl-v">openargs</span> <span class="pl-k">=</span> args[<span class="pl-c1">0</span>]

    <span class="pl-c"># check here</span>
    <span class="pl-k">if</span> <span class="pl-k">!</span>openargs.name
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Database name value is missing in openDatabase call<span class="pl-pds">'</span></span>

    <span class="pl-k">if</span> <span class="pl-k">!</span>openargs.iosDatabaseLocation <span class="pl-k">and</span> <span class="pl-k">!</span>openargs.location <span class="pl-k">and</span> openargs.location <span class="pl-k">isnt</span> <span class="pl-c1">0</span>
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Database location or iosDatabaseLocation value is now mandatory in openDatabase call<span class="pl-pds">'</span></span>

    <span class="pl-c"># XXX TODO (with test):</span>
    <span class="pl-c">#if !!openargs.location and !!openargs.iosDatabaseLocation</span>
    <span class="pl-c">#  throw newSQLError 'Abiguous: both location or iosDatabaseLocation values are present in openDatabase call'</span>

    <span class="pl-v">dblocation</span> <span class="pl-k">=</span>
      <span class="pl-k">if</span> <span class="pl-k">!!</span>openargs.location <span class="pl-k">and</span> openargs.location <span class="pl-k">is</span> <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>
        iosLocationMap[<span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>]
      <span class="pl-k">else</span> <span class="pl-k">if</span> <span class="pl-k">!!</span>openargs.iosDatabaseLocation
        iosLocationMap[openargs.iosDatabaseLocation]
      <span class="pl-k">else</span>
        dblocations[openargs.location]

    <span class="pl-c"># XXX TODO (with test):</span>
    <span class="pl-c">#if !dblocation</span>
    <span class="pl-c">#  throw newSQLError 'Valid iOS database location could not be determined in openDatabase call'</span>

    openargs.<span class="pl-v">dblocation</span> <span class="pl-k">=</span> dblocation

    <span class="pl-k">if</span> <span class="pl-k">!!</span>openargs.createFromLocation <span class="pl-k">and</span> openargs.createFromLocation <span class="pl-k">==</span> <span class="pl-c1">1</span>
      openargs.<span class="pl-v">createFromResource</span> <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>

    <span class="pl-k">if</span> <span class="pl-k">!!</span>openargs.androidDatabaseImplementation <span class="pl-k">and</span> openargs.androidDatabaseImplementation <span class="pl-k">==</span> <span class="pl-c1">2</span>
      openargs.<span class="pl-v">androidOldDatabaseImplementation</span> <span class="pl-k">=</span> <span class="pl-c1">1</span>

    <span class="pl-k">if</span> <span class="pl-k">!!</span>openargs.androidLockWorkaround <span class="pl-k">and</span> openargs.androidLockWorkaround <span class="pl-k">==</span> <span class="pl-c1">1</span>
      openargs.<span class="pl-v">androidBugWorkaround</span> <span class="pl-k">=</span> <span class="pl-c1">1</span>

    <span class="pl-v">okcb</span> <span class="pl-k">=</span> <span class="pl-c1">null</span>
    <span class="pl-v">errorcb</span> <span class="pl-k">=</span> <span class="pl-c1">null</span>
    <span class="pl-k">if</span> args.length <span class="pl-k">&gt;=</span> <span class="pl-c1">2</span>
      <span class="pl-v">okcb</span> <span class="pl-k">=</span> args[<span class="pl-c1">1</span>]
      <span class="pl-k">if</span> args.length <span class="pl-k">&gt;</span> <span class="pl-c1">2</span> <span class="pl-k">then</span> <span class="pl-v">errorcb</span> <span class="pl-k">=</span> args[<span class="pl-c1">2</span>]

    <span class="pl-k">new</span> <span class="pl-en">SQLitePlugin</span> openargs, okcb, errorcb

  <span class="pl-en">deleteDatabase</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(first, success, error)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    <span class="pl-v">args</span> <span class="pl-k">=</span> {}

    <span class="pl-k">if</span> first.constructor <span class="pl-k">==</span> <span class="pl-c1">String</span>
      <span class="pl-c">#console.log "delete db name: #{first}"</span>
      <span class="pl-c">#args.path = first</span>
      <span class="pl-c">#args.dblocation = dblocations[0]</span>
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Sorry first deleteDatabase argument must be an object<span class="pl-pds">'</span></span>

    <span class="pl-k">else</span>
      <span class="pl-c">#console.log "delete db args: #{JSON.stringify first}"</span>
      <span class="pl-k">if</span> <span class="pl-k">!</span>(first <span class="pl-k">and</span> first[<span class="pl-s"><span class="pl-pds">'</span>name<span class="pl-pds">'</span></span>]) <span class="pl-k">then</span> <span class="pl-k">throw</span> <span class="pl-k">new</span> <span class="pl-en">Error</span> <span class="pl-s"><span class="pl-pds">"</span>Please specify db name<span class="pl-pds">"</span></span>
      args.<span class="pl-v">path</span> <span class="pl-k">=</span> first.name
      <span class="pl-c">#dblocation = if !!first.location then dblocations[first.location] else null</span>
      <span class="pl-c">#args.dblocation = dblocation || dblocations[0]</span>

    <span class="pl-k">if</span> <span class="pl-k">!</span>first.iosDatabaseLocation <span class="pl-k">and</span> <span class="pl-k">!</span>first.location <span class="pl-k">and</span> first.location <span class="pl-k">isnt</span> <span class="pl-c1">0</span>
      <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Database location or iosDatabaseLocation value is now mandatory in deleteDatabase call<span class="pl-pds">'</span></span>

    <span class="pl-c"># XXX TODO (with test):</span>
    <span class="pl-c">#if !!first.location and !!first.iosDatabaseLocation</span>
    <span class="pl-c">#  throw newSQLError 'Abiguous: both location or iosDatabaseLocation values are present in deleteDatabase call'</span>

    <span class="pl-v">dblocation</span> <span class="pl-k">=</span>
      <span class="pl-k">if</span> <span class="pl-k">!!</span>first.location <span class="pl-k">and</span> first.location <span class="pl-k">is</span> <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>
        iosLocationMap[<span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>]
      <span class="pl-k">else</span> <span class="pl-k">if</span> <span class="pl-k">!!</span>first.iosDatabaseLocation
        iosLocationMap[first.iosDatabaseLocation]
      <span class="pl-k">else</span>
        dblocations[first.location]

    <span class="pl-c"># XXX TODO (with test):</span>
    <span class="pl-c">#if !dblocation</span>
    <span class="pl-c">#  throw newSQLError 'Valid iOS database location could not be determined in deleteDatabase call'</span>

    args.<span class="pl-v">dblocation</span> <span class="pl-k">=</span> dblocation

    <span class="pl-c"># XXX [BUG #210] TODO: when closing or deleting a db, abort any pending transactions (with error callback)</span>
    <span class="pl-k">delete</span> SQLitePlugin<span class="pl-k">::</span>openDBs[args.path]
    cordova.<span class="pl-en">exec</span> success, error, <span class="pl-s"><span class="pl-pds">"</span>SQLitePlugin<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>delete<span class="pl-pds">"</span></span>, [ args ]</pre></div>

<h2><a id="user-content-self-test" class="anchor" href="#self-test" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>Self test:</h2>

<div class="highlight highlight-source-coffee"><pre><span class="pl-v">SelfTest</span> <span class="pl-k">=</span>
  <span class="pl-v">DBNAME</span>: <span class="pl-s"><span class="pl-pds">'</span>___$$$___litehelpers___$$$___test___$$$___.db<span class="pl-pds">'</span></span>

  <span class="pl-en">start</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(successcb, errorcb)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    SQLiteFactory.<span class="pl-en">deleteDatabase</span> {<span class="pl-v">name</span>: SelfTest.DBNAME, <span class="pl-v">location</span>: <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>},
      (<span class="pl-k">-&gt;</span> SelfTest.<span class="pl-en">start2</span>(successcb, errorcb)),
      (<span class="pl-k">-&gt;</span> SelfTest.<span class="pl-en">start2</span>(successcb, errorcb))

  <span class="pl-en">start2</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(successcb, errorcb)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    SQLiteFactory.<span class="pl-en">openDatabase</span> {<span class="pl-v">name</span>: SelfTest.DBNAME, <span class="pl-v">location</span>: <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>}, <span class="pl-smi">(db)</span> <span class="pl-k">-&gt;</span>
      db.<span class="pl-en">sqlBatch</span> [
        <span class="pl-s"><span class="pl-pds">'</span>CREATE TABLE TestTable(TestColumn);<span class="pl-pds">'</span></span>
        [ <span class="pl-s"><span class="pl-pds">'</span>INSERT INTO TestTable (TestColumn) VALUES (?);<span class="pl-pds">'</span></span>, [<span class="pl-s"><span class="pl-pds">'</span>test-value<span class="pl-pds">'</span></span>] ]
      ], <span class="pl-smi">()</span> <span class="pl-k">-&gt;</span>
        db.<span class="pl-en">executeSql</span> <span class="pl-s"><span class="pl-pds">'</span>SELECT * FROM TestTable<span class="pl-pds">'</span></span>, [], <span class="pl-smi">(resutSet)</span> <span class="pl-k">-&gt;</span>
          <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet.rows
            SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows<span class="pl-pds">'</span></span>
            <span class="pl-k">return</span>

          <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet.rows.length
            SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows.length<span class="pl-pds">'</span></span>
            <span class="pl-k">return</span>

          <span class="pl-k">if</span> resutSet.rows.length <span class="pl-k">isnt</span> <span class="pl-c1">1</span>
            SelfTest.<span class="pl-en">finishWithError</span> errorcb,
              <span class="pl-s"><span class="pl-pds">"</span>Incorrect resutSet.rows.length value: <span class="pl-s1"><span class="pl-pse">#{</span>resutSet.rows.length<span class="pl-pse">}</span></span> (expected: 1)<span class="pl-pds">"</span></span>
            <span class="pl-k">return</span>

          <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn
            SelfTest.<span class="pl-en">finishWithError</span> errorcb,
              <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows.item(0).TestColumn<span class="pl-pds">'</span></span>
            <span class="pl-k">return</span>

          <span class="pl-k">if</span> resutSet.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn <span class="pl-k">isnt</span> <span class="pl-s"><span class="pl-pds">'</span>test-value<span class="pl-pds">'</span></span>
            SelfTest.<span class="pl-en">finishWithError</span> errorcb,
              <span class="pl-s"><span class="pl-pds">"</span>Incorrect resutSet.rows.item(0).TestColumn value: <span class="pl-s1"><span class="pl-pse">#{</span>resutSet.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn<span class="pl-pse">}</span></span> (expected: 'test-value')<span class="pl-pds">"</span></span>
            <span class="pl-k">return</span>

          db.transaction <span class="pl-smi">(tx)</span> <span class="pl-k">-&gt;</span>
            tx.<span class="pl-en">executeSql</span> <span class="pl-s"><span class="pl-pds">'</span>UPDATE TestTable SET TestColumn = ?<span class="pl-pds">'</span></span>, [<span class="pl-s"><span class="pl-pds">'</span>new-value<span class="pl-pds">'</span></span>]
          , <span class="pl-smi">(tx_err)</span> <span class="pl-k">-&gt;</span>
            SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>UPDATE transaction error: <span class="pl-s1"><span class="pl-pse">#{</span>tx_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>
          , <span class="pl-smi">()</span> <span class="pl-k">-&gt;</span>
            db.readTransaction <span class="pl-smi">(tx2)</span> <span class="pl-k">-&gt;</span>
              tx2.<span class="pl-en">executeSql</span> <span class="pl-s"><span class="pl-pds">'</span>SELECT * FROM TestTable<span class="pl-pds">'</span></span>, [], <span class="pl-smi">(ignored, resutSet2)</span> <span class="pl-k">-&gt;</span>
                <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet2.rows
                  <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows<span class="pl-pds">'</span></span>

                <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet2.rows.length
                  <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows.length<span class="pl-pds">'</span></span>

                <span class="pl-k">if</span> resutSet2.rows.length <span class="pl-k">isnt</span> <span class="pl-c1">1</span>
                  <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>Incorrect resutSet.rows.length value: <span class="pl-s1"><span class="pl-pse">#{</span>resutSet.rows.length<span class="pl-pse">}</span></span> (expected: 1)<span class="pl-pds">"</span></span>

                <span class="pl-k">if</span> <span class="pl-k">!</span>resutSet2.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn
                  <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">'</span>Missing resutSet.rows.item(0).TestColumn<span class="pl-pds">'</span></span>

                <span class="pl-k">if</span> resutSet2.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn <span class="pl-k">isnt</span> <span class="pl-s"><span class="pl-pds">'</span>new-value<span class="pl-pds">'</span></span>
                  <span class="pl-k">throw</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>Incorrect resutSet.rows.item(0).TestColumn value: <span class="pl-s1"><span class="pl-pse">#{</span>resutSet.rows.<span class="pl-en">item</span>(<span class="pl-c1">0</span>).TestColumn<span class="pl-pse">}</span></span> (expected: 'test-value')<span class="pl-pds">"</span></span>

            , <span class="pl-smi">(tx2_err)</span> <span class="pl-k">-&gt;</span>
              SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>readTransaction error: <span class="pl-s1"><span class="pl-pse">#{</span>tx2_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>
            , <span class="pl-smi">()</span> <span class="pl-k">-&gt;</span>
              <span class="pl-c"># CLEANUP &amp; FINISH:</span>
              db.close <span class="pl-smi">()</span> <span class="pl-k">-&gt;</span>
                SQLiteFactory.<span class="pl-en">deleteDatabase</span> {<span class="pl-v">name</span>: SelfTest.DBNAME, <span class="pl-v">location</span>: <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>}, successcb, <span class="pl-smi">(cleanup_err)</span><span class="pl-k">-&gt;</span>
                  SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>Cleanup error: <span class="pl-s1"><span class="pl-pse">#{</span>cleanup_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>

              , <span class="pl-smi">(close_err)</span> <span class="pl-k">-&gt;</span>
                SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>close error: <span class="pl-s1"><span class="pl-pse">#{</span>close_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>

        , <span class="pl-smi">(select_err)</span> <span class="pl-k">-&gt;</span>
          SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>SELECT error: <span class="pl-s1"><span class="pl-pse">#{</span>select_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>

      , <span class="pl-smi">(batch_err)</span> <span class="pl-k">-&gt;</span>
        SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>sql batch error: <span class="pl-s1"><span class="pl-pse">#{</span>batch_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>

    , <span class="pl-smi">(open_err)</span> <span class="pl-k">-&gt;</span>
      SelfTest.<span class="pl-en">finishWithError</span> errorcb, <span class="pl-s"><span class="pl-pds">"</span>Open database error: <span class="pl-s1"><span class="pl-pse">#{</span>open_err<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span>

  <span class="pl-en">finishWithError</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(errorcb, message)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    SQLiteFactory.<span class="pl-en">deleteDatabase</span> {<span class="pl-v">name</span>: SelfTest.DBNAME, <span class="pl-v">location</span>: <span class="pl-s"><span class="pl-pds">'</span>default<span class="pl-pds">'</span></span>}, <span class="pl-k">-&gt;</span>
      <span class="pl-en">errorcb</span> <span class="pl-en">newSQLError</span> message
    , <span class="pl-smi">(err2)</span><span class="pl-k">-&gt;</span> <span class="pl-en">errorcb</span> <span class="pl-en">newSQLError</span> <span class="pl-s"><span class="pl-pds">"</span>Cleanup error: <span class="pl-s1"><span class="pl-pse">#{</span>err2<span class="pl-pse">}</span></span> for error: <span class="pl-s1"><span class="pl-pse">#{</span>message<span class="pl-pse">}</span></span><span class="pl-pds">"</span></span></pre></div>

<h2><a id="user-content-exported-api" class="anchor" href="#exported-api" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>Exported API:</h2>

<div class="highlight highlight-source-coffee"><pre>root.<span class="pl-v">sqlitePlugin</span> <span class="pl-k">=</span>
  <span class="pl-v">sqliteFeatures</span>:
    <span class="pl-v">isSQLitePlugin</span>: <span class="pl-c1">true</span>

  <span class="pl-en">echoTest</span><span class="pl-k">:</span><span class="pl-smi"> <span class="pl-smi">(okcb, errorcb)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
    <span class="pl-en">ok</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(s)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
      <span class="pl-k">if</span> s <span class="pl-k">is</span> <span class="pl-s"><span class="pl-pds">'</span>test-string<span class="pl-pds">'</span></span>
        <span class="pl-en">okcb</span>()
      <span class="pl-k">else</span>
        <span class="pl-en">errorcb</span> <span class="pl-s"><span class="pl-pds">"</span>Mismatch: got: '<span class="pl-s1"><span class="pl-pse">#{</span>s<span class="pl-pse">}</span></span>' expected 'test-string'<span class="pl-pds">"</span></span>

    <span class="pl-en">error</span> <span class="pl-k">=</span><span class="pl-smi"> <span class="pl-smi">(e)</span></span> <span class="pl-k"><span class="pl-k">-&gt;</span></span>
      <span class="pl-en">errorcb</span> e

    cordova.<span class="pl-en">exec</span> okcb, errorcb, <span class="pl-s"><span class="pl-pds">"</span>SQLitePlugin<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>echoStringValue<span class="pl-pds">"</span></span>, [{<span class="pl-v">value</span>:<span class="pl-s"><span class="pl-pds">'</span>test-string<span class="pl-pds">'</span></span>}]

  <span class="pl-v">selfTest</span>: SelfTest.start

  <span class="pl-v">openDatabase</span>: SQLiteFactory.openDatabase
  <span class="pl-v">deleteDatabase</span>: SQLiteFactory.deleteDatabase</pre></div>

<h2><a id="user-content-vim-directives" class="anchor" href="#vim-directives" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>vim directives</h2>

<h4><a id="user-content-vim-set-filetypecoffee-" class="anchor" href="#vim-set-filetypecoffee-" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>vim: set filetype=coffee :</h4>

<h4><a id="user-content-vim-set-expandtab-" class="anchor" href="#vim-set-expandtab-" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1h-1c-1.5 0-3-1.69-3-3.5s1.55-3.5 3-3.5h4c1.45 0 3 1.69 3 3.5 0 1.41-0.91 2.72-2 3.25v-1.16c0.58-0.45 1-1.27 1-2.09 0-1.28-1.02-2.5-2-2.5H4c-0.98 0-2 1.22-2 2.5s1 2.5 2 2.5z m9-3h-1v1h1c1 0 2 1.22 2 2.5s-1.02 2.5-2 2.5H9c-0.98 0-2-1.22-2-2.5 0-0.83 0.42-1.64 1-2.09v-1.16c-1.09 0.53-2 1.84-2 3.25 0 1.81 1.55 3.5 3 3.5h4c1.45 0 3-1.69 3-3.5s-1.5-3.5-3-3.5z"></path></svg></a>vim: set expandtab :</h4>
</article>
  </div>

</div>

<button type="button" data-facebox="#jump-to-line" data-facebox-class="linejump" data-hotkey="l" class="hidden">Jump to Line</button>
<div id="jump-to-line" style="display:none">
  <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="" class="js-jump-to-line-form" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <input class="form-control linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
    <button type="submit" class="btn">Go</button>
</form></div>

  </div>
  <div class="modal-backdrop"></div>
</div>


    </div>
  </div>

    </div>

        <div class="container site-footer-container">
  <div class="site-footer" role="contentinfo">
    <ul class="site-footer-links right">
        <li><a href="https://status.github.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
      <li><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
      <li><a href="https://shop.github.com" data-ga-click="Footer, go to shop, text:shop">Shop</a></li>
        <li><a href="https://github.com/blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a href="https://github.com/about" data-ga-click="Footer, go to about, text:about">About</a></li>

    </ul>

    <a href="https://github.com" aria-label="Homepage" class="site-footer-mark" title="GitHub">
      <svg aria-hidden="true" class="octicon octicon-mark-github" height="24" version="1.1" viewBox="0 0 16 16" width="24"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59 0.4 0.07 0.55-0.17 0.55-0.38 0-0.19-0.01-0.82-0.01-1.49-2.01 0.37-2.53-0.49-2.69-0.94-0.09-0.23-0.48-0.94-0.82-1.13-0.28-0.15-0.68-0.52-0.01-0.53 0.63-0.01 1.08 0.58 1.23 0.82 0.72 1.21 1.87 0.87 2.33 0.66 0.07-0.52 0.28-0.87 0.51-1.07-1.78-0.2-3.64-0.89-3.64-3.95 0-0.87 0.31-1.59 0.82-2.15-0.08-0.2-0.36-1.02 0.08-2.12 0 0 0.67-0.21 2.2 0.82 0.64-0.18 1.32-0.27 2-0.27 0.68 0 1.36 0.09 2 0.27 1.53-1.04 2.2-0.82 2.2-0.82 0.44 1.1 0.16 1.92 0.08 2.12 0.51 0.56 0.82 1.27 0.82 2.15 0 3.07-1.87 3.75-3.65 3.95 0.29 0.25 0.54 0.73 0.54 1.48 0 1.07-0.01 1.93-0.01 2.2 0 0.21 0.15 0.46 0.55 0.38C13.71 14.53 16 11.53 16 8 16 3.58 12.42 0 8 0z"></path></svg>
</a>
    <ul class="site-footer-links">
      <li>&copy; 2016 <span title="0.13505s from github-fe154-cp1-prd.iad.github.net">GitHub</span>, Inc.</li>
        <li><a href="https://github.com/site/terms" data-ga-click="Footer, go to terms, text:terms">Terms</a></li>
        <li><a href="https://github.com/site/privacy" data-ga-click="Footer, go to privacy, text:privacy">Privacy</a></li>
        <li><a href="https://github.com/security" data-ga-click="Footer, go to security, text:security">Security</a></li>
        <li><a href="https://github.com/contact" data-ga-click="Footer, go to contact, text:contact">Contact</a></li>
        <li><a href="https://help.github.com" data-ga-click="Footer, go to help, text:help">Help</a></li>
    </ul>
  </div>
</div>



    

    <div id="ajax-error-message" class="ajax-error-message flash flash-error">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M15.72 12.5l-6.85-11.98C8.69 0.21 8.36 0.02 8 0.02s-0.69 0.19-0.87 0.5l-6.85 11.98c-0.18 0.31-0.18 0.69 0 1C0.47 13.81 0.8 14 1.15 14h13.7c0.36 0 0.69-0.19 0.86-0.5S15.89 12.81 15.72 12.5zM9 12H7V10h2V12zM9 9H7V5h2V9z"></path></svg>
      <button type="button" class="flash-close js-flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
        <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48-3.75-3.75-3.75 3.75-1.48-1.48 3.75-3.75L0.77 4.25l1.48-1.48 3.75 3.75 3.75-3.75 1.48 1.48-3.75 3.75z"></path></svg>
      </button>
      Something went wrong with that request. Please try again.
    </div>


      
      <script crossorigin="anonymous" integrity="sha256-52zkLOd8k0WG98rL4k1Vbb5v79votTo5NkSxgZn3wpE=" src="https://assets-cdn.github.com/assets/frameworks-e76ce42ce77c934586f7cacbe24d556dbe6fefdbe8b53a393644b18199f7c291.js"></script>
      <script async="async" crossorigin="anonymous" integrity="sha256-NANhFHarpUSfevcS2/e0iLu1UuCj6TxV02wFj+eWi0Y=" src="https://assets-cdn.github.com/assets/github-3403611476aba5449f7af712dbf7b488bbb552e0a3e93c55d36c058fe7968b46.js"></script>
      
      
      
      
      
      
    <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner hidden">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M15.72 12.5l-6.85-11.98C8.69 0.21 8.36 0.02 8 0.02s-0.69 0.19-0.87 0.5l-6.85 11.98c-0.18 0.31-0.18 0.69 0 1C0.47 13.81 0.8 14 1.15 14h13.7c0.36 0 0.69-0.19 0.86-0.5S15.89 12.81 15.72 12.5zM9 12H7V10h2V12zM9 9H7V5h2V9z"></path></svg>
      <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
      <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
    </div>
    <div class="facebox" id="facebox" style="display:none;">
  <div class="facebox-popup">
    <div class="facebox-content" role="dialog" aria-labelledby="facebox-header" aria-describedby="facebox-description">
    </div>
    <button type="button" class="facebox-close js-facebox-close" aria-label="Close modal">
      <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48-3.75-3.75-3.75 3.75-1.48-1.48 3.75-3.75L0.77 4.25l1.48-1.48 3.75 3.75 3.75-3.75 1.48 1.48-3.75 3.75z"></path></svg>
    </button>
  </div>
</div>

  </body>
</html>

