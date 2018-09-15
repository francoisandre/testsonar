
<!DOCTYPE html>
<!--[if IE 9 ]> <html class="ie9"> <![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--> <html> <!--<![endif]-->
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <link rel="shortcut icon" type="image/x-icon" href="/images/favicon.ico?1497362122">
  
  <title>SonarQube - mapi-gin-gestion-des-contrats-des-non-titulaires</title>

  <link href="/css/sonarnoadmin.css?v=5.5" rel="stylesheet" media="all">
  
  <script>
    var pageLang = 'fr';
    
    window.SS = {
      hoursInDay: 8,
      user: '',
      userName: '',
      userEmail: '',
      lf: {
        enableGravatar: true,
        gravatarServerUrl: 'https://secure.gravatar.com/avatar/{EMAIL_MD5}.jpg?s={SIZE}&d=identicon'
      },
      updateCenterActive: true
    };
  </script>
  <script src="/js/bundles/vendor.js?v=5.5"></script>
  <script src="/js/bundles/sonar.js?v=5.5"></script>
  <script>
    window.baseUrl = '';
  </script>
  
  <script src="/js/bundles/dashboard.js?v=5.5"></script>
  <script src="/js/bundles/widgets.js?v=5.5"></script>
</head>
<body>


  
<div class="page-wrapper page-wrapper-context" id="container">
  <nav class="navbar navbar-global page-container" id="global-navigation"></nav>

  
    <nav class="navbar navbar-context page-container" id="context-navigation"></nav>
  

  
  <div id="body" class="page-container">
    <div id="content">
      <div class="panel hidden" id="messages-panel">
        <div class="alert alert-danger hidden" id="error">
          <span id="errormsg"></span> &nbsp;&nbsp;[<a href="#" onclick="return hideError();">hide</a>]
        </div>
        <div class="alert alert-info hidden" id="info">
          <span id="infomsg"></span> &nbsp;&nbsp;[<a href="#" onclick="return hideInfo();">hide</a>]
        </div>
        <div class="alert alert-warning hidden" id="warning">
          <span id="warningmsg"></span> &nbsp;&nbsp;[<a href="#" onclick="return hideWarning();">hide</a>]
        </div>
      </div>
      


<div class="page" id="dashboard">
    <span class="hidden" id="is-project-dashboard">&nbsp;</span>
    <header class="page-header">
  <h1 class="page-title">Dashboard</h1>


  <div class="page-actions noprint">
    
      
        
        
          <form method="GET" action="/dashboard/index/531075" style="display: inline" class="spacer-left">
            <input type="hidden" name="did" value="3"/>
            <select id="select-comparison" name="period" onchange="submit()"><option selected value='0' class='small'/>Time changes...</option><option value='1'  class='small'>&Delta; since previous version (13.100.0.2-SNAPSHOT - 11 sept. 2018)</option><option value='2'  class='small'>&Delta; since previous analysis (11 sept. 2018)</option><option value='3'  class='small'>&Delta; over 30 days (21 août 2018)</option></select><script>$j(document).ready(function() {$j('#select-comparison').select2({minimumResultsForSearch:344,allowClear:false,placeholder:'',width:'250px'});});</script>          </form>
        
      
    

    
  </div>
</header>

  <div style="width: 100%;display: block; float: none">
    
      <!-- the right margin with 1px is a trick for IE. See SONAR-2637 -->
      <div class="dashboard-column-wrapper" style="width: 50%;margin: 0 -1px 0 0;">
        <div class="dashboard-column" id="dashboard-column-1" style="margin: 0 5px 0 0px;">
          
              


  <div class="block" id="block_125">
    

    <div class="alerts" style="height:100%;">
      
        <div class="widget color_WARN" style="color: black !important" id="quality_gate_widget_125">
  <div><span id='m_alert_status'  ><i class="icon-alert-warn"></i></span> The project has warnings on the following quality gate conditions: </div>
            <div class="dashbox" style="margin: 10px; vertical-align: baseline">
        <p class="title">Coverage</p>
        
          <span class="big" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom"><a href="/drilldown/measures/531075?metric=coverage" class='widget-link ' rel='' title=''><span id='m_coverage' class='alert_WARN' >6,4%</span></a></span>
        
        < <span id='m_coverage'  >65,0%</span>                        <p></p>
      </div>
          <div class="dashbox" style="margin: 10px; vertical-align: baseline">
        <p class="title">Major issues</p>
        
          <span class="big" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom"><a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=MAJOR" class='widget-link ' rel='' title=''><span id='m_major_violations' class='alert_WARN' >28</span></a></span>
        
        > <span id='m_major_violations'  >10</span>                        <p></p>
      </div>
    </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_105">
    

    <div class="events" style="height:100%;">
      
        <div class="widget">
          

<script type="text/javascript">
  function changeCategory(categoryId, widgetId) {
    var eventTableMaxSize = 8;
    $j('#events_' + widgetId + ' tr.event').hide();
    var elements;
    if (categoryId=='all') {
      elements = $j('#events_' + widgetId + ' tr.event');
    } else {
      elements = $j('#events_' + widgetId + ' tr.cat_' + categoryId);
    }
    var elementsToDisplay = elements.slice(0,eventTableMaxSize);
    if (elementsToDisplay.size()==0) {
      $j('#events_' + widgetId).hide();
      $j('#show_more_events_' + widgetId).hide();
      $j('#no_event_message_' + widgetId).show();
    } else {
      $j('#events_' + widgetId).show();
      $j('#no_event_message_' + widgetId).hide();
      elementsToDisplay.show();
      if (elements.size() > eventTableMaxSize) {
        $j('#show_more_events_' + widgetId).show();
      } else {
        $j('#show_more_events_' + widgetId).hide();
      }
    }
  }

  function showAllEvents(widgetId) {
    var selectedCategory = $j('#select_category_' + widgetId).val();
    if (selectedCategory=='all') {
      $j('#events_' + widgetId + ' tr.event').show();
    } else {
      $j('#events_' + widgetId + ' tr.cat_' + selectedCategory).show();
    }
    $j('#show_more_events_' + widgetId).hide();
  }
</script>


<h3>Events &nbsp;&nbsp;

  <select class="small" id="select_category_105" onchange="changeCategory(this.value, 105);">
    <option value="all">All</option>
    
    <option value="alert">Quality Gate</option>
    
    <option value="other">Other</option>
    
    <option value="profile">Quality Profile</option>
    
    <option value="version">Version</option>
    
  </select>

  <script>
    $j(function() {
      $j('#select_category_105').select2({ width: '150px' });
    });
  </script>

</h3>

<table id="events_105" class="spaced data">
  <thead>
    <tr>
      <th colspan="4"></th>
    </tr>
  </thead>

  <tbody>

<tr class="even event cat_version">
    <td x="Thu Sep 13 23:15:11 +0200 2018">13 sept. 2018</td>
    <td>Version</td>
    <td>
      13.300.0.0-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="odd event cat_version">
    <td x="Tue Sep 11 22:09:21 +0200 2018">11 sept. 2018</td>
    <td>Version</td>
    <td>
      13.100.0.2-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="even event cat_version">
    <td x="Thu Aug 23 23:20:08 +0200 2018">23 août 2018</td>
    <td>Version</td>
    <td>
      13.100.0.1-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="odd event cat_version">
    <td x="Wed Aug 22 22:47:10 +0200 2018">22 août 2018</td>
    <td>Version</td>
    <td>
      12.300.0.0-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="even event cat_version">
    <td x="Tue Aug 21 16:09:30 +0200 2018">21 août 2018</td>
    <td>Version</td>
    <td>
      12.300.0.2-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="odd event cat_alert">
    <td x="Mon Jul 30 14:54:50 +0200 2018">30 juil. 2018</td>
    <td>Quality Gate</td>
    <td>
      Orange (was Red)    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Major issues &gt; 10"></i>
      
    </td>
</tr>

<tr class="even event cat_alert">
    <td x="Mon Jul 30 14:38:40 +0200 2018">30 juil. 2018</td>
    <td>Quality Gate</td>
    <td>
      Red (was Orange)    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Critical issues &gt; 0, Major issues &gt; 10"></i>
      
    </td>
</tr>

<tr class="odd event cat_alert">
    <td x="Mon Jul 30 14:38:10 +0200 2018">30 juil. 2018</td>
    <td>Quality Gate</td>
    <td>
      Orange (was Red)    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Major issues &gt; 10"></i>
      
    </td>
</tr>

<tr class="even event cat_alert">
    <td x="Sat Jul 28 01:11:30 +0200 2018">28 juil. 2018</td>
    <td>Quality Gate</td>
    <td>
      Red (was Orange)    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Critical issues &gt; 0, Major issues &gt; 10"></i>
      
    </td>
</tr>

<tr class="odd event cat_version">
    <td x="Tue Jun 19 00:10:36 +0200 2018">19 juin 2018</td>
    <td>Version</td>
    <td>
      12.200.0.0-SNAPSHOT    </td>
    <td>
      
    </td>
</tr>

<tr class="even event cat_alert">
    <td x="Wed Jun 13 23:52:11 +0200 2018">13 juin 2018</td>
    <td>Quality Gate</td>
    <td>
      Orange (was Red)    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Major issues &gt; 10"></i>
      
    </td>
</tr>

<tr class="odd event cat_alert">
    <td x="Thu May 24 10:13:41 +0200 2018">24 mai 2018</td>
    <td>Quality Gate</td>
    <td>
      Red    </td>
    <td>
      
        <i class="icon-info" title="Coverage &lt; 65, Critical issues &gt; 0, Major issues &gt; 10"></i>
      
    </td>
</tr>

  </tbody>
</table>

<div id="no_event_message_105" style="margin: 5px">
  <span class="empty_widget">No event</span>
</div>

<a href="#" onclick="showAllEvents(105);return false;" id="show_more_events_105" class="action">Show All</a>

<script type="text/javascript">
  changeCategory('all', 105);
</script>


          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_28">
    

    <div class="size" style="height:100%;">
      
        <div class="widget">
          

<div class="widget-row widget-row-x">

  <div class="widget-span widget-span-3-5">
    <div class="widget-measure-container">
      
        <p class="widget-measure widget-measure-main">
          <span class="widget-label">Lines of code</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=ncloc" class='widget-link ' rel='' title=''><span id='m_ncloc'  >5 821</span></a>
                      </span>
        </p>
        

        
          
            
                            Java            
          
        
      
    </div>
  </div>

  <div class="widget-span widget-span-3-5">
    <div class="widget-measure-container">
      <p class="widget-measure widget-measure-main">
        <span class="widget-label">Files</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=files" class='widget-link ' rel='' title=''><span id='m_files'  >64</span></a>
                  </span>
      </p>

      
        <p class="widget-measure">
          <span class="widget-label">Directories</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=directories" class='widget-link ' rel='' title=''><span id='m_directories'  >15</span></a>
                      </span>
        </p>
      

      <p class="widget-measure">
        <span class="widget-label">Lines</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=lines" class='widget-link ' rel='' title=''><span id='m_lines'  >14 359</span></a>
                  </span>
      </p>

      

      
    </div>
  </div>

  <div class="widget-span widget-span-5">
    <div class="widget-measure-container">
      
        <p class="widget-measure widget-measure-main">
          <span class="widget-label">Functions</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=functions" class='widget-link ' rel='' title=''><span id='m_functions'  >426</span></a>
                      </span>
        </p>
      

      
        <p class="widget-measure">
          <span class="widget-label">Classes</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=classes" class='widget-link ' rel='' title=''><span id='m_classes'  >63</span></a>
                      </span>
        </p>
      

      
        <p class="widget-measure">
          <span class="widget-label">Statements</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=statements" class='widget-link ' rel='' title=''><span id='m_statements'  >2 158</span></a>
                      </span>
        </p>
      

      
        <p class="widget-measure">
          <span class="widget-label">Accessors</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?metric=accessors" class='widget-link ' rel='' title=''><span id='m_accessors'  >351</span></a>
                      </span>
        </p>
      
    </div>
  </div>

</div>

          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_25">
    

    <div class="documentation_comments" style="height:100%;">
      
        <div class="widget">
          
<div class="widget-row">
  <div class="widget-span widget-span-6">
    
    <div class="widget-measure-container">
      
      <div class="widget-measure widget-measure-main">
        <span class="widget-label">Documentation</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?highlight=public_documented_api_density&amp;metric=public_undocumented_api" class='widget-link ' rel='' title=''><span id='m_public_documented_api_density' class='alert_OK' >99,7%</span></a>
                  </span>
      </div>
      
      <div class="widget-measure">
        <span class="widget-label">Public API</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=public_api" class='widget-link ' rel='' title=''><span id='m_public_api'  >342</span></a>
                  </span>
      </div>
      <div class="widget-measure">
        <span class="widget-label">Pub. undoc. API</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=public_undocumented_api" class='widget-link ' rel='' title=''><span id='m_public_undocumented_api'  >1</span></a>
                  </span>
      </div>
    </div>
    
  </div>

  <div class="widget-span widget-span-6">
    <div class="widget-measure-container">
      <div class="widget-measure widget-measure-main">
        <span class="widget-label">Comments</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=comment_lines_density" class='widget-link ' rel='' title=''><span id='m_comment_lines_density'  >36,0%</span></a>
                  </span>
      </div>
      <div class="widget-measure">
        <span class="widget-label">Comment lines</span>
        <span class="nowrap">
          <a href="/drilldown/measures/531075?metric=comment_lines" class='widget-link ' rel='' title=''><span id='m_comment_lines'  >3 278</span></a>
                  </span>
      </div>
    </div>
  </div>
</div>

          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_31">
    

    <div class="rules" style="height:100%;">
      
        <div class="widget">
          

<div class="widget-row">

  <div class="widget-span widget-span-3">
    <div class="widget-measure-container">
      <div class="widget-measure widget-measure-main">
        <span class="widget-label">Issues</span>
        <span class="nowrap">
          <span class="link-rules-issues">
            <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires" class="widget-link link-rules-debt"
               title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
              <span id='m_violations'  >253</span>            </a>
          </span>
                  </span>
      </div>
      <div class="widget-measure-delta">
        
      </div>
    </div>
  </div>

  <div class="widget-span widget-span-3">
    
      <div class="widget-measure">
        <span class="widget-label">Technical Debt</span>
        <a href="/drilldown/measures/531075?metric=sqale_index" class="widget-link link-rules-debt"
           title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
          <span id='m_sqale_index'  >29d</span>        </a>
              </div>
      <div class="widget-measure-delta">
        
      </div>
    

    
      <div class="widget-measure">
        <span class="widget-label">Reliability Remediation Effort</span>
        <a href="/drilldown/measures/531075?metric=reliability_remediation_effort" class="widget-link"
           title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
          <span id='m_reliability_remediation_effort'  >0</span>        </a>
              </div>
      <div class="widget-measure-delta">
        
      </div>
    

    
      <div class="widget-measure">
        <span class="widget-label">Security Remediation Effort</span>
        <a href="/drilldown/measures/531075?metric=security_remediation_effort" class="widget-link"
           title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
          <span id='m_security_remediation_effort'  >10min</span>        </a>
              </div>
      <div class="widget-measure-delta">
        
      </div>
    
  </div>

  <div class="widget-span widget-span-4">
    <table class="data widget-barchar">
      <tr>
        <td class="thin nowrap">
          <i class="icon-severity-blocker"></i>
          Blocker        </td>
        <td class="thin right nowrap">
          <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=BLOCKER"
             class="widget-link drilldown_BLOCKER" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
            <span id='m_blocker_violations' class='alert_OK' >0</span>          </a>
        </td>
        <td class="thin nowrap">
          
        </td>
      </tr>
      <tr>
        <td class="thin nowrap">
          <i class="icon-severity-critical"></i>
          Critical        </td>
        <td class="thin right nowrap">
          <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=CRITICAL"
             class="widget-link drilldown_CRITICAL" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
            <span id='m_critical_violations' class='alert_OK' >0</span>          </a>
        </td>
        <td class="thin nowrap">
          
        </td>
      </tr>
      <tr>
        <td class="thin nowrap">
          <i class="icon-severity-major"></i>
          Major        </td>
        <td class="thin right nowrap">
          <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=MAJOR"
             class="widget-link drilldown_MAJOR" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
            <span id='m_major_violations' class='alert_WARN' >28</span>          </a>
        </td>
        <td class="thin nowrap">
          
        </td>
      </tr>
      <tr>
        <td class="thin nowrap">
          <i class="icon-severity-minor"></i>
          Minor        </td>
        <td class="thin right nowrap">
          <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=MINOR"
             class="widget-link drilldown_MINOR" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
            <span id='m_minor_violations'  >225</span>          </a>
        </td>
        <td class="thin nowrap">
          
        </td>
      </tr>
      <tr>
        <td class="thin nowrap">
          <i class="icon-severity-info"></i>
          Info        </td>
        <td class="thin right nowrap">
          <a href="/component_issues?id=fr.gouv.education.sirhen.mapi%3Amapi-gin-gestion-des-contrats-des-non-titulaires#resolved=false|severities=INFO"
             class="widget-link drilldown_INFO" title="As calculated on 13 sept. 2018 23:15" data-toggle="tooltip" data-placement="bottom">
            <span id='m_info_violations'  >0</span>          </a>
        </td>
        <td class="thin nowrap">
          
        </td>
      </tr>
    </table>
  </div>
</div>
          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
        </div>
      </div>
    
      <!-- the right margin with 1px is a trick for IE. See SONAR-2637 -->
      <div class="dashboard-column-wrapper" style="width: 50%;margin: 0 -1px 0 0;">
        <div class="dashboard-column" id="dashboard-column-2" style="margin: 0 0px 0 5px;">
          
              


  <div class="block" id="block_33">
    

    <div class="complexity" style="height:100%;">
      
        <div class="widget">
          

  <div class="widget-row">
    <div class="widget-span widget-span-5">
      <div class="widget-measure-container">
        
          <p class="widget-measure widget-measure-main">
            <span class="widget-label">Complexity</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=complexity" class='widget-link ' rel='' title=''><span id='m_complexity'  >950</span></a>
                          </span>
          </p>
        
        
          <p class="widget-measure">
            <span class="widget-label"> /function</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=function_complexity" class='widget-link ' rel='' title=''><span id='m_function_complexity'  >2,2</span></a>
                          </span>
          </p>
        
        
          <p class="widget-measure">
            <span class="widget-label"> /class</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=class_complexity" class='widget-link ' rel='' title=''><span id='m_class_complexity'  >15,1</span></a>
                            </span>
          </p>
        
        
          <p class="widget-measure">
            <span class="widget-label"> /file</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=file_complexity" class='widget-link ' rel='' title=''><span id='m_file_complexity'  >14,8</span></a>
                            </span>
          </p>
        
      </div>
    </div>

    <div class="widget-span widget-span-7">
      
        <div id="complexity-widget-33-function-distribution"></div>
        <script>
          (function () {
            window.ComplexityDistribution({
              el: '#complexity-widget-33-function-distribution',
              value: '1=228;2=53;4=42;6=19;8=10;10=5;12=9',
              of: 'function'
            });
            })();
        </script>
      
      
      <div id="complexity-widget-33-file-distribution"></div>
      <script>
        (function () {
          window.ComplexityDistribution({
            el: '#complexity-widget-33-file-distribution',
            value: '0=25;5=13;10=16;20=2;30=3;60=3;90=2',
            of: 'file'
          });
          })();
      </script>
      
    </div>
  </div>

          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_32">
    

    <div class="code_coverage" style="height:100%;">
      
        <div class="widget">
          
  <div class="widget-row">
    <div class="widget-span widget-span-6">
      <div class="widget-measure-container">
        <div class="widget-measure widget-measure-main">
          <span class="widget-label">Unit Tests Coverage</span>
          <span class="nowrap">
            <a href="/drilldown/measures/531075?highlight=coverage&amp;metric=uncovered_lines" class='widget-link ' rel='Coverage &lt; 65' title='Coverage &lt; 65'><span id='m_coverage' class='alert_WARN' >6,4%</span></a>
                      </span>
        </div>
        
          <div class="widget-measure">
            <span class="widget-label"> line coverage</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?highlight=line_coverage&amp;metric=uncovered_lines" class='widget-link ' rel='' title=''><span id='m_line_coverage'  >7,6%</span></a>
                          </span>
          </div>
        
        
          <div class="widget-measure">
            <span class="widget-label"> condition coverage</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?highlight=branch_coverage&amp;metric=uncovered_conditions" class='widget-link ' rel='' title=''><span id='m_branch_coverage'  >2,7%</span></a>
                          </span>
          </div>
        

        
      </div>
    </div>
    <div class="widget-span widget-span-6">
      
        <div class="widget-measure-container">
          <div class="widget-measure widget-measure-main">
            <span class="widget-label">Unit test success</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=test_success_density" class='widget-link ' rel='' title=''><span id='m_test_success_density' class='alert_OK' >100,0%</span></a>
                          </span>
          </div>

          <div class="widget-measure">
            <span class="widget-label"> failures</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=test_failures" class='widget-link ' rel='' title=''><span id='m_test_failures'  >0</span></a>
                          </span>
          </div>

          <div class="widget-measure">
            <span class="widget-label"> errors</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=test_errors" class='widget-link ' rel='' title=''><span id='m_test_errors'  >0</span></a>
                          </span>
          </div>

          <div class="widget-measure">
            <span class="widget-label"> tests</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=tests" class='widget-link ' rel='' title=''><span id='m_tests'  >14</span></a>
                          </span>
          </div>

          
            <div class="widget-measure">
              <span class="widget-label"> skipped</span>
              <span class="nowrap">
                <a href="/drilldown/measures/531075?metric=skipped_tests" class='widget-link ' rel='' title=''><span id='m_skipped_tests'  >3</span></a>
                              </span>
            </div>
          

          <div class="widget-measure">
            <span class="widget-label">Execution Time</span>
            <span class="nowrap">
              <a href="/drilldown/measures/531075?metric=test_execution_time" class='widget-link ' rel='' title=''><span id='m_test_execution_time'  >979 ms</span></a>
                          </span>
          </div>
        </div>
      
    </div>
  </div>

          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
              


  <div class="block" id="block_100">
    

    <div class="duplications" style="height:100%;">
      
        <div class="widget">
          
<div class="widget-row">
  <div class="widget-span widget-span-12">
    <div class="widget-measure widget-measure-main">
      <span class="widget-label">Duplications</span>
      <span class="nowrap">
        <a href="/drilldown/measures/531075?highlight=duplicated_lines_density&amp;metric=duplicated_lines" class='widget-link ' rel='' title=''><span id='m_duplicated_lines_density' class='alert_OK' >2,0%</span></a>
              </span>
    </div>

    <div class="widget-measure">
      <span class="widget-label"> lines</span>
      <span class="nowrap">
        <a href="/drilldown/measures/531075?metric=duplicated_lines" class='widget-link ' rel='' title=''><span id='m_duplicated_lines'  >287</span></a>
              </span>
    </div>

    <div class="widget-measure">
      <span class="widget-label"> blocks</span>
      <span class="nowrap">
        <a href="/drilldown/measures/531075?metric=duplicated_blocks" class='widget-link ' rel='' title=''><span id='m_duplicated_blocks'  >11</span></a>
              </span>
    </div>

    <div class="widget-measure">
      <span class="widget-label"> files</span>
      <span class="nowrap">
        <a href="/drilldown/measures/531075?metric=duplicated_files" class='widget-link ' rel='' title=''><span id='m_duplicated_files'  >5</span></a>
              </span>
    </div>

  </div>
</div>

          <div class="clear"></div>
        </div>
      

      <div style="clear: both;"></div>
    </div>
  </div>




          
        </div>
      </div>
    
  </div>
  <div style="clear: both;"></div>
</div>

<script>
  jQuery('html').addClass('dashboard-page');
  jQuery('[data-toggle="tooltip"]').tooltip({ container: '#body' });
</script>

    </div>
  </div>
</div>


  
  <div id="footer" class="page-footer page-container">
    
    
    <div>SonarQube&trade; technology is powered by <a href="http://www.sonarsource.com" target="SonarSource SA">SonarSource SA</a></div>
    <div>
      Version 5.5 -
      <a href="http://www.gnu.org/licenses/lgpl-3.0.txt" target="lgpl_v3">LGPL v3</a> -
      <a href="http://www.sonarqube.org" target="sonar">Community</a> -
      <a href="http://www.sonarqube.org/documentation" target="sonar_doc">Documentation</a> -
      <a href="http://www.sonarqube.org/support" target="support">Get Support</a> -
      <a href="http://redirect.sonarsource.com/doc/plugin-library.html" target="plugins">Plugins</a> -
      <a href="/web_api">Web API</a>
    </div>
    <!--[if lte IE 8 ]><p class="spacer-top alert alert-danger">IE 8 is not supported. Some widgets may not be properly displayed. Please switch to a <a target="_blank" href="http://redirect.sonarsource.com/doc/requirements.html">supported version or another supported browser</a>.</p><!--<![endif]-->
  </div>


  

<script>
  (function () {
    
    window.sonarqube.space = 'component';
    window.sonarqube.componentKey = 'fr.gouv.education.sirhen.mapi:mapi-gin-gestion-des-contrats-des-non-titulaires';
    

    

    window.SS.isUserAdmin = false;
  })();
</script>


<!--[if lte IE 7 ]>
<div style="position:fixed;z-index:99999;top:0;bottom:0;left:0;right:0;background:#fff;">
  <div style="margin-top:150px;text-align:center;line-height:1.4;color:#333;">
    The web interface cannot be displayed because your browser is not supported.<br>
    Please switch to a <a target="_blank"
                          href="http://redirect.sonarsource.com/doc/requirements.html">supported version or another supported browser</a>.
  </div>
</div>
<!--<![endif]-->



<script src="/js/bundles/main.js?v=5.5"></script>

</body>
</html>
