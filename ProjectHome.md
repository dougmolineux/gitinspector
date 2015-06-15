gitinspector is a statistical analysis tool for git repositories. The defaut analysis shows general statistics per author, which can be complemented with a timeline analysis that shows the workload and activity of each author. Under normal operation, it filters the results to only show statistics about a number of given extensions and by default only includes source files in the statistical analysis.

This tool was originally written to help fetch repository statistics from student projects in the course [Object-oriented Programming Project (TDA367/DIT211)](http://www.cse.chalmers.se/edu/course/TDA367/) at Chalmers University of Technology and Gothenburg University.

Today, gitinspector is used as a grading aid by universities worldwide.


<a href='http://wiki.gitinspector.googlecode.com/git/images/html_example.jpg'><img src='http://wiki.gitinspector.googlecode.com/git/images/html_example_thumbnail.jpg' align='right' /></a>

# Features #

  * Shows cumulative work by each author in the history.
  * Filters results by extension (default: java,c,cc,cpp,h,hh,hpp,py,glsl,rb,js,sql).
  * Can display a statistical timeline analysis.
  * Scans for all filetypes (by extension) found in the repository.
  * Multi-threaded; uses multiple instances of git to speed up analysis when possible.
  * Supports HTML, XML and plain text output (console).
  * Can report violations of different code metrics.

# Example outputs #

Below are some example outputs for a number of famous open source projects. All the statistics were generated using the "-HTlr" flags.

| Django | [HTML](http://wiki.gitinspector.googlecode.com/git/examples/django_output.html) | [HTML Embedded](http://wiki.gitinspector.googlecode.com/git/examples/django_output.emb.html) | [Plain Text](http://wiki.gitinspector.googlecode.com/git/examples/django_output.txt) |[XML](http://wiki.gitinspector.googlecode.com/git/examples/django_output.xml) |
|:-------|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| JQuery | [HTML](http://wiki.gitinspector.googlecode.com/git/examples/jquery_output.html) | [HTML Embedded](http://wiki.gitinspector.googlecode.com/git/examples/jquery_output.emb.html) | [Plain Text](http://wiki.gitinspector.googlecode.com/git/examples/jquery_output.txt) | [XML](http://wiki.gitinspector.googlecode.com/git/examples/jquery_output.xml) |
| Pango  | [HTML](http://wiki.gitinspector.googlecode.com/git/examples/pango_output.html)  | [HTML Embedded](http://wiki.gitinspector.googlecode.com/git/examples/pango_output.emb.html)  | [Plain Text](http://wiki.gitinspector.googlecode.com/git/examples/pango_output.txt)  | [XML](http://wiki.gitinspector.googlecode.com/git/examples/pango_output.xml) |

# Another example of output from gitinspector #

Below is an example of the ouput generated by gitinspector:

```
$ ./gitinspector.py -wTHl /path/to/some/git/repository
The following historical commit information, by author, was found in the repository:

Author               Commits   Insertions   Deletions   % of changes
John Smith               288         7721        4617          39.19
James Johnson            135         8910        2422          35.99
Robert Brown              71         2564        1352          12.44
Michael Davids           134         2943         954          12.38

Below are the number of rows from each author that have survived and are still intact in the current revision:

Author                     Rows   % in comments
John Smith                 3533           22.02
James Johnson              6113           52.15
Robert Brown               1123           21.19
Michael Davids             1464           20.15

The following history timeline has been gathered from the repository:

Author                  2012W37    2012W38    2012W39    2012W40    2012W41    2012W42    2012W43
John Smith             --++++++      --+++   --++++++       -+++   ---+++++  ----+++++          .
James Johnson                 +   -+++++++       ++++  -++++++++       --++     --++++   -+++++++
Robert Brown                         --+++          +          .       -+++          +          .
Michael Davids                         +++         ++          +          +          +          .
Modified Rows:             1522       3832       7553       6143       5833       5123       1477            

The extensions below were found in the repository history (extensions used during statistical analysis are marked):
xml [java] pdf txt css
```

The above output shows a timeline where "+" depicts added lines and "-" depicts removed lines. A "." means that there were changes by that author during that week but the amount of work was very small in relation to the rest of the work that week.

The number of signs in no way describes the size of the work, rather, it is the amount of work each week in relation to the other authors.

# The Team #
  * Adam Waldenberg, Lead maintainer and Swedish translation
  * Bill Wang, Chinese translation
  * Christian Kastner, Debian package maintainer
  * Jiwon Kim, Korean translation
  * Kamila Chyla, Polish translation
  * Luca Motta, Italian translation
  * Philipp Nowak, German translation
  * Sergei Lomakov, Russian translation
  * Yannick Moy, French translation
We need translations for gitinspector! If you are a gitinspector user, feel willing to help and have good language skills in any unsupported language we urge you to contact us. We also happily accept code patches. Please refer to [Contributing](Contributing.md) for more information on how to contribute to the project.

# License #

gitinspector is licensed under the GNU GPL v3.
The gitinspector logo is partly based on the git logo; based on the work of Jason Long. The logo is licensed under the Creative Commons Attribution 3.0 Unported License.

&lt;wiki:gadget url="http://www.ohloh.net/p/605990/widgets/project\_basic\_stats.xml" height="220" width="450" border="0"/&gt;