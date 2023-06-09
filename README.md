# want-some-linux

<html lang="en">
<head>
    <meta content="text/html; charset=utf-8" http-equiv="Content-Type">
    <title>Code Quality</title>

    <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,300,700' rel='stylesheet' type='text/css'>
    <link href='https://fonts.googleapis.com/css?family=PT+Serif:400,700,400italic' rel='stylesheet' type='text/css'>
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.css" rel="stylesheet">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">

    <link href="css/metricsgraphics.css" rel="stylesheet" type="text/css" id="light">
    <link href="css/metricsgraphics-dark.css" rel="stylesheet" type="text/css" id="dark">
    <link href="css/code-quality.css" rel="stylesheet" type="text/css">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.4.11/d3.min.js" charset="utf-8"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js"></script>
    <script src='js/metricsgraphics.min.js'></script>
    <script>
      (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
      (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
      m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
      })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

      ga('create', 'UA-49796218-24', 'auto');
      ga('send', 'pageview');
    </script>
</head>
<body>
    <div class='container'>
        <div class='row'>
            <div class='col-lg-12 text-center'>
                <h1 class='text-center'>Code Quality</h1>
                <p class='text-center'>Architectural measures of complexity for revisions in <a href='https://hg.mozilla.org/mozilla-central/'>mozilla-central</a>. Click on a data point to view details about that revision. 
                Other things you might be interested in doing with the data from the latest revision&mdash;the address will change once <a href='https://bugzilla.mozilla.org/show_bug.cgi?id=1224318'>this bug</a> is resolved.</p>
                <a href='http://almossawi.com:3003/deps/filename=accessible:jsat:EventManager.jsm'>1. View a file's dependencies</a> &nbsp; &nbsp;
                <a href='http://almossawi.com:3003/functions/filename=accessible:jsat:EventManager.jsm'>2. View a file's function-level metrics</a>

                <ul class='switch text-center'>
                    <li><a href='#' id='goto-all' class='pill'>All modules</a></li>
                </ul>
                <ul class='timescale text-center'>
                    <li><a href='#' id='monthly' class='pill active'>Monthly</a></li>
                    <li><a href='#' id='daily' class='pill'>Daily</a></li>
                </ul>
            </div>
        </div>
        <div class='row'>
            <div class='col-lg-4 text-center chart' id='loc'></div>
            <div class='col-lg-4 text-center chart' id='files'></div>
            <div class='col-lg-4 text-center chart' id='mccabe'></div>
        </div>
        <div class='row'>
            <div class='col-lg-4 text-center chart' id='dependencies'></div>
            <div class='col-lg-4 text-center chart' id='prop-cost'></div>
            <div class='col-lg-4 text-center chart' id='core'></div>
        </div>
        <div class='revision-data text-center'>
            Hover over the data points below to see details about individual revisions.
        </div>
    </div>
    <div class='footer text-center'>
        <a href='https://github.com/mozilla/firefox-code-quality'>Code and documentation</a>
        <br /><a href="https://metrics.mozilla.com/quality-indices">See the Quality Indices interface</a>
        <br /><a href="https://github.com/mozilla/metrics-graphics">
            <i class="fa fa-github fa-3x" style="line-height:42px"></i>
        </a>
    </div>
    <script src='js/main.js'></script>
</body>
</html>
