<h1>Index Controller</h1>
<p>Welcome to MOZART index controller.</p>

<h2>Download</h2>
<p>You can download MOZART from github.</p>
<p>Clone from github:
</p>
<blockquote>
<code>git clone git://github.com/krbi12/MOZART-MVC.git</code>
</blockquote>
<p>You can review its source directly on github and download from there: <a href='https://github.com/krbi12/MOZART-MVC'>https://github.com/krbi12/MOZART-MVC</a></p>

<h2>Installation</h2>
<p>After you have downloaded MOZART and uploaded it to your webserver you have to make the data-directory writable. This is the location of the database where content is stored and updated, and thus the place where MOZART needs
to be able to write and create files.</p>
<blockquote>
<code>cd lydia; chmod 777 site/data</code>
</blockquote>

<p>
Secondly, MOZART uses mod_rewrite, and in order to make links work correctly you might have to modify the .htaccess-file. If the links don't work as expected, uncomment line 4 in .htaccess and specify the path so it corresponds to the path of your MOZART-installation. If your MOZART-files are located in a directory called MOZART, directly in the root of your webserver, line 4 should look like this:
<blockquote>
RewriteBase /MOZART/
</blockquote>
</p>

<p>Finally, MOZART has some modules that need to be initialised. You can do this through a 
controller. Point your browser to the following link.</p>
<blockquote>
Example: http://example.com/modules/install
</blockquote>

<h2>Post installation</h2>
<ul>
<li>
<h3>Configuration</h3>
<p>Basic configuration is done in the file <span class="directory">site/config.php</span>. Information about how to use it is found in the file.
</p>
</li>
<li>
<h3>Theming</h3>
<p>Themes for MOZART are located in the directory <span class="directory">themes/</span>. Theme files can also be placed in <span class="directory">site/themes/</span>, and a neat way to use this feature is to let the theme in <span class="directory">site/themes/</span> use a theme in <span class="directory">themes/</span> as a parent theme. This is done in the default installation of MOZART, where the theme 'mozart' (<span class="directory">site/themes/mozart/</span>) uses the theme found in <span class="directory">themes/grid/</span> as a parent theme. This allows you to do simple changes to the theme in the small and easily editable file <span class="directory">site/themes/mozart/style.css</span>. If you want to do a big makeover of the sites appearance, you should make a copy of one of the theme directories in <span class="directory">themes/</span>, give it a new name and create your custom theme in this new directory. In this case, you will also have to edit the following lines in <span class="directory"
>site/config.php</span> so it points to the correct theme.
<blockquote>
$ly->config['theme'] = array(<br />
  'path'            => <strong>'site/themes/mozart'</strong>,<br />
  'parent'          => <strong>'themes/grid'</strong>,<br />
  'stylesheet'      => <strong>'style.css'</strong>,
</blockquote>
</p>
</li>
<li>
<h3>Logo</h3>
<p>Open <span class="directory">site/config.php</span> in an editor and change the following lines (at the very end of the file) so it corresponds to your logo image. Make sure that the path to your image is set correctly. In the default installation of MOZART, the following lines points to the image 'logo_80x80.png' located in <span class="directory">site/themes/mozart/</span>.
<blockquote>
'favicon' => <strong>'logo_80x80.png'</strong>,<br />
    'logo' => <strong>'logo_80x80.png'</strong>,<br />
    'logo_width'  => <strong>80</strong>,<br />
    'logo_height' => <strong>80</strong>,
</blockquote>
</p>
</li>
<li>
<h3>Title</h3>
<p>Open <span class="directory">site/config.php</span> and edit the following line at the very end of the file.
<blockquote>
    'header' => <strong>'MOZART'</strong>,<br />
    'slogan' => <strong>'Learning MVC'</strong>,
</blockquote>
</p>
</li>
<li>
<h3>Footer</h3>
<p>Open <span class="directory">site/config.php</span> and edit the following line at the very end of the file.
<blockquote>
    'footer' => '<strong><p>MOZART &copy; by Krister Birgersson (krister.birgersson@gmail.com), based on Lydia by Mos (mos@dbwebb.se)'</p></strong>
</blockquote>
</p>
</li>
<li>
<h3>Navigation</h3>
<p>There are two hardcoded menus availible in the default installation. To set which one should be used, comment out one of the two following lines in <span class="directory">site/config.php</span> (at the very end of the file).
<blockquote>
  'menu_to_region' => array('navbar'=>'navbar'),<br />
//  'menu_to_region' => array('my-navbar'=>'navbar'),
</blockquote>
You can also edit the availible menus or define new ones. To do that, open <span class="directory">site/config.php</span> and edit the array following this line:
<blockquote>
$ly->config['menus'] = array(
</blockquote>
</p>
</li>
</ul>
<p>
Good luck with installing MOZART! I hope you will enjoy using it.
</p>
