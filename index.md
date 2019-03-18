---
layout: workshop      # DON'T CHANGE THIS.
carpentry: ""
venue: "The Jackson Laboratory"
address: "Breezeway Bioinformatics Training Room 1540, Building 1, Unit 5, 600 Main St, Bar Harbor ME"
country: "us"
language: "en"
latlng: "44.365336,-68.196283"
humandate: "May 21, 2018"
humantime: "9:00 am - 3:00 pm"
startdate: 2019-05-21
enddate: 2019-05-21
instructor: ["Rich Brey", "Sue McClatchy"]
helper: ["FIXME"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["susan.mcclatchy@jax.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:
---
{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
frameborder="0"
width="100%"
height="280px"
scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
{% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
This workshop is only open to Jackson Laboratory employees.
{% if page.carpentry == "swc" %}
{% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
<strong>Where:</strong>
{{page.address}}.
Get directions with
<a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
or
<a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
<strong>When:</strong>
{{page.humandate}}.
{% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
<strong>Requirements:</strong> Participants must bring a laptop with a
Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.). They should have a few specific software packages installed (listed
<a href="#setup">below</a>).
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Code of Conduct:</strong>  Everyone who participates is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>.
</p>

{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
<strong>Accessibility:</strong> We are committed to making this workshop
accessible to everybody.
The workshop organizers have checked that:
</p>
<ul>
<li>The room is wheelchair / scooter accessible.</li>
<li>Accessible restrooms are available.</li>
</ul>
<p>
Materials will be provided in advance of the workshop and
large-print handouts are available if needed by notifying the
organizers in advance.  If we can help making learning easier for
you (e.g. sign-language interpreters, lactation facilities) please
get in touch (using contact details below) and we will
attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
<strong>Contact</strong>:
Please email
{% if page.email %}
{% for email in page.email %}
{% if forloop.last and page.email.size > 1 %}
or
{% else %}
{% unless forloop.first %}
,
{% endunless %}
{% endif %}
<a href='mailto:{{email}}'>{{email}}</a>
{% endfor %}
{% else %}
to-be-announced
{% endif %}
for more information.
</p>

<hr/>

{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>
<div class="row">
<div class="col-md-6">
<h3>Day 1</h3>
<table class="table table-striped">
<tr> <td>Before</td> <td><a href="https://www.surveymonkey.com/r/J95QZGY">Pre-workshop survey</a> </td> </tr>
<tr> <td>09:00</td>  <td>Welcome and introductions</td> </tr>
<tr> <td>09:15</td>  <td><a href="https://swcarpentry.github.io/shell-novice/01-intro/index.html">Introducing the Shell</a></td> </tr>
<tr> <td>09:20</td>  <td><a href="https://swcarpentry.github.io/shell-novice/02-filedir/index.html">Navigating Files and Directories</a></td> </tr>
<tr> <td>10:00</td>  <td><a href="https://swcarpentry.github.io/shell-novice/03-create/index.html">Working With Files and Directories</a></td> </tr>
<tr> <td>10:30</td>  <td>Coffee</td> </tr>
<tr> <td>10:45</td>  <td><a href="https://swcarpentry.github.io/shell-novice/03-create/index.html">Working With Files and Directories (continued)</a></td> </tr>
<tr> <td>11:05</td>  <td><a href="https://swcarpentry.github.io/shell-novice/04-pipefilter/index.html">Pipes and Filters</a></td> </tr>
<tr> <td>12:00</td>  <td>Lunch break</td> </tr>
<tr> <td>13:00</td>  <td>Introduction to JAX High Performance Computing</td> </tr>
<tr> <td>14:45</td>  <td><a href="https://www.surveymonkey.com/r/XDHJ6S5">Post-workshop survey</a> </td> </tr>
<tr> <td>15:00</td>  <td>END</td> </tr>
</table>
</div>
</div>


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.software-carpentry.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

{% include sc/syllabus.html %}


<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
To participate in a
{% if page.carpentry == "swc" %}
Software Carpentry
{% elsif page.carpentry == "dc" %}
Data Carpentry
{% elsif page.carpentry == "lc" %}
Library Carpentry
{% endif %}
workshop,
you will need access to the software described below.
In addition, you will need an up-to-date web browser.
</p>

<div id="shell"> {% comment %} Start of 'shell' section. {% endcomment %}
<h3>The Bash Shell</h3>

<p>
Bash is a commonly-used shell that gives you the power to do simple
tasks more quickly.
</p>

<div class="row">
<div class="col-md-4">
<h4 id="shell-windows">Windows</h4>
<ol>
<li>Ask the JAX IT Service Desk to download and install <a href="https://putty.org/">PuTTY</a>.</li>
</ol>
</div>
<div class="col-md-4">
<h4 id="shell-macosx">macOS</h4>
<p>
The default shell in all versions of macOS is Bash, so no
need to install anything.  You access Bash from the Terminal
(found in
<code>/Applications/Utilities</code>).
See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
for an example on how to open the Terminal.
You may want to keep
Terminal in your dock for this workshop.
</p>
</div>
<div class="col-md-4">
<h4 id="shell-linux">Linux</h4>
<p>
The default shell is usually Bash, but if your
machine is set up differently you can run it by opening a
terminal and typing <code>bash</code>.  There is no need to
install anything.
</p>
</div>
</div> {% comment %} End of 'shell' section. {% endcomment %}


<div id="editor"> {% comment %} Start of 'editor' section. {% endcomment %}
<h3>Text Editor</h3>

<p>
When you're writing code, it's nice to have a text editor that is
optimized for writing code, with features like automatic
color-coding of key words.  The default text editor on macOS and
Linux is usually set to Vim, which is not famous for being
intuitive.  If you accidentally find yourself stuck in it, try
typing the escape key, followed by <code>:q!</code> (colon, lower-case 'q',
exclamation mark), then hitting Return to return to the shell.
</p>

<div class="row">
<div class="col-md-4">
<h4 id="editor-windows">Windows</h4>
<p>
nano is a basic editor and the default that instructors use in the workshop.
It is installed along with Git.
</p>
<p>
Others editors that you can use are
<a href="https://notepad-plus-plus.org/">Notepad++</a> or
<a href="https://www.sublimetext.com/">Sublime Text</a>.
<strong>Be aware that you must
add its installation directory to your system path.</strong>
Please ask your instructor to help you do this.
</p>
</div>
<div class="col-md-4">
<h4 id="editor-macosx">macOS</h4>
<p>
nano is a basic editor and the default that instructors use in the workshop.
See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
for an example on how to open nano.
It should be pre-installed.
</p>
<p>
Others editors that you can use are
<a href="https://www.barebones.com/products/textwrangler/">Text Wrangler</a> or
<a href="https://www.sublimetext.com/">Sublime Text</a>.
</p>
</div>
<div class="col-md-4">
<h4 id="editor-linux">Linux</h4>
<p>
nano is a basic editor and the default that instructors use in the workshop.
It should be pre-installed.
</p>
<p>
Others editors that you can use are
<a href="https://wiki.gnome.org/Apps/Gedit">Gedit</a>,
<a href="https://kate-editor.org/">Kate</a> or
<a href="https://www.sublimetext.com/">Sublime Text</a>.
</p>
</div>
</div>
</div> {% comment %} End of 'editor' section. {% endcomment %}

<div id="cluster"> {% comment %} Start of 'cluster' section. {% endcomment %}
<h3>High Performance Computing Cluster</h3>
<p>
JAX provides access to high performance computing (HPC) through two computing clusters:
1) Cadillac, which serves Bar Harbor; and
2) Helix, which serves Farmington.
</p>
<div class="row">
<div class="col-md-4">
<h4 id="shell-windows">Cluster Access</h4>
Ask the JAX IT Service Desk to give you an account for Cadillac (Bar Harbor) or Helix (Farmington).
</div>
</div>
</div> {% comment %} End of 'cluster' section. {% endcomment %}

