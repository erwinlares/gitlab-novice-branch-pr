---
layout: page
title: Setup
permalink: /setup/
---

<div id="shell">
  <h3>The Bash Shell</h3>
  <p>
    Bash is a commonly-used shell that gives you the power to do
    tasks more quickly.
  </p>

  <div>
    <ul class="nav nav-tabs" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#shell-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#shell-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#shell-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>
    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="shell-windows">
        <ol>
          <li>Download the Git for Windows <a href="https://gitforwindows.org/">installer</a>.</li>
          <li>Run the installer and follow the steps below:
            <ol>
              {% comment %} Git 2.29.1 Setup {% endcomment %}
              <li>
                Click on "Next" four times (two times if you've previously
                installed Git).  You don't need to change anything
                in the Information, location, components, and start menu screens.
              </li>
              <li>
                <strong>
                  From the dropdown menu, "Choosing the default editor used by Git", select "Use the Nano editor by default" (NOTE: you will need to scroll <emph>up</emph> to find it) and click on "Next".
                </strong>
              </li>
              {% comment %} Adjusting the name of the initial branch in new repositories {% endcomment %}
              <li>
                On the page that says "Adjusting the name of the initial branch in new repositories", ensure that
		"Let Git decide" is selected. This will ensure the highest level of compatibility for our lessons.
		{% comment %}
		This section also has "Override the default branch name for new repositories" and has a text box set
		to "main". I'm not having people switch to this just yet because our git lesson still uses the old paradigm.
		{% endcomment %}     
              </li>
              {% comment %} Adjusting your PATH environment {% endcomment %}
              <li>
                Ensure that "Git from the command line and also from 3rd-party software" is selected and
                click on "Next". (If you don't do this Git Bash will not work properly, requiring you to
                remove the Git Bash installation, re-run the installer and to select the "Git from the
                command line and also from 3rd-party software" option.)
              </li>
              {% comment %} Choosing the SSH executable {% endcomment %}
 	      <li>
	      Select "Use bundled OpenSSH".
	      </li>
              {% comment %} Choosing HTTPS transport backend {% endcomment %}
              <li>
		Ensure that "Use the native Windows Secure Channel Library" is selected and click on "Next".
	      </li>
              {% comment %} This should mean that people stuck behind corporate firewalls that do MITM attacks
                                 with their own root CA are still able to access remote git repos. {% endcomment %}
              {% comment %} Configuring the line ending conversions {% endcomment %}
              <li>
                Ensure that "Checkout Windows-style, commit Unix-style line endings" is selected and click on "Next".
              </li>
              {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}
              <li>
                <strong>
                  Ensure that "Use Windows' default console window" is selected and click on "Next".
                </strong>
              </li>
              {% comment %} Configuring extra options {% endcomment %}
              <li>
		Ensure that "Default (fast-forward or merge) is selected and click "Next"
              </li>
              <li>
		Ensure that "Git Credential Manager" is selected and click on "Next".
              </li>
              <li>
		Ensure that "Enable file system caching" is selected and click on "Next".
              </li>
              {% comment %} Configuring experimental options {% endcomment %}
              <li>Click on "Install".</li>
              {% comment %} Installing {% endcomment %}
              {% comment %} Completing the Git Setup Wizard {% endcomment %}
              {% comment %} as of 2020-06-02, the Window will say "click Finish", but the button is labelled as "Next" {% endcomment %}
              <li>Click on "Finish" or "Next".</li>
            </ol>
          </li>
          <li>
            If your "HOME" environment variable is not set (or you don't know what this is):
            <ol>
              <li>Open command prompt (Open Start Menu then type <code>cmd</code> and press <kbd>Enter</kbd>)</li>
              <li>
                Type the following line into the command prompt window exactly as shown:
                <p><code>setx HOME "%USERPROFILE%"</code></p>
              </li>
              <li>Press <kbd>Enter</kbd>, you should see <code>SUCCESS: Specified value was saved.</code></li>
              <li>Quit command prompt by typing <code>exit</code> then pressing <kbd>Enter</kbd></li>
            </ol>
	  </li>
        </ol>
        <p>This will provide you with both Git and Bash in the Git Bash program.</p>
      </article>
      <article role="tabpanel" class="tab-pane" id="shell-macos">
        <p>
          You already have bash or zshell installed as part of macOS and can use that for learning the Unix shell.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane" id="shell-linux">
        <p>
          The default shell is usually Bash and there is usually no need to
          install anything.
        </p>
        <p>
          To see if your default shell is Bash type <code>echo $SHELL</code> in
          a terminal and press the <kbd>Enter</kbd> key. If the message printed
          does not end with '/bash' then your default is something else and you
          can run Bash by typing <code>bash</code>.
        </p>
      </article>
    </div>
  </div>
</div>

{% comment %}
Git Setup instructions rely on Shell instructions. If you don't include
Shell instructions as part of your workshop website, make sure to adjust
the text below accordingly.
{% endcomment %}
<div id="git">
  <h3>Git</h3>
  <p>
    Git is a version control system that lets you track who made changes
    to what when and has options for easily updating a shared or public
    version of your code
    on GitLab. You will need a web browser.
  </p>
  <p>
    You will need an account at <a href="https://git.doit.wisc.edu/">the UW GitLab instance</a>
    for parts of the Git lesson. An account should be provisioned for you when you log in with your
    netid.  See the <a href="https://kb.wisc.edu/shared-tools/page.php?id=121442">Gitlab Knowledgebase</a>
    for additional information about setting up an account.  
  </p>

  <div>
    <ul class="nav nav-tabs" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#git-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#git-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#git-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>
    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="git-windows">
        <p>
          Git should be installed on your computer as part of your Bash
          install (see the
          <a href="#shell">Shell installation instructions</a>).
        </p>
      </article>
      <article role="tabpanel" class="tab-pane" id="git-macos">
        <p>
          Please open the Terminal app, type <code>git --version</code> and press 
          <kbd>Enter</kbd>/<kbd>Return</kbd>. If it's not installed already, 
          follow the instructions to <code>Install</code> the "command line 
          developer tools". <strong>Do not click</strong> "Get Xcode", because that will 
          take too long and is not necessary for our Git lesson.
          After installing these tools, there won't be anything in your <code>/Applications</code>
          folder, as they and Git are command line programs.
          <strong>For older versions of OS X (10.5-10.8)</strong> use the
          most recent available installer labelled "snow-leopard"
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
          (Note: this project is no longer maintained.)
          Because this installer is not signed by the developer, you may have to
          right click (control click) on the .pkg file, click Open, and click
          Open in the pop-up dialog.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane" id="git-linux">
        <p>
          If Git is not already available on your machine you can try to
          install it via your distro's package manager. For Debian/Ubuntu run
          <code>sudo apt-get install git</code> and for Fedora run
          <code>sudo dnf install git</code>.
        </p>
      </article>
    </div>
  </div>
</div>

[workshop-setup]: https://swcarpentry.github.io/workshop-template/#git
