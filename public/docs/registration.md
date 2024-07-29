<!DOCTYPE html>
<html lang="en" id="oranda" class="axo">
  <head>
    <title>aws-keychain</title>
    
    
      <link rel="icon" href="/aws-keychain/favicon.ico" />
    
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    
      <meta name="description" content="A simple, lightweight, and fast static site generator." />
      <meta property="og:description" content="A simple, lightweight, and fast static site generator." />
    
    <meta property="og:type" content="website" />
    <meta property="og:title" content="aws-keychain" />
    
    
    
    <meta http-equiv="Permissions-Policy" content="interest-cohort=()" />
    <link rel="stylesheet" href="/aws-keychain/oranda-v0.6.1.css" />
    
    
  </head>
  <body>
    <div class="container">
      <div class="page-body">
        
          <div class="repo_banner">
            <a href="https://github.com/acn-gen-tomita/binary-zone">
              <div class="github-icon" aria-hidden="true"></div>
              Check out our GitHub!
            </a>
          </div>
        

        <main>
          <header>
            
            <h1 class="title">aws-keychain</h1>
            
  <nav class="nav">
    <ul>
      <li><a href="/aws-keychain/">Home</a></li>

      
        
          <li><a href="/aws-keychain/docs/registration/">Register Account</a></li>
        
      

      
        <li><a href="/aws-keychain/artifacts/">Install</a></li>
      

      

      

      
        <li><a href="/aws-keychain/changelog/">Changelog</a></li>
      
    </ul>
  </nav>

          </header>

          
  
    <h2>Setup Login</h2>
<p>To use the <code>aws-keychain</code> command, you need to register an AWS account. Prepare the following information before running the command:</p>
<ol>
<li>URL of the account (e.g. <a href="https://accounts.google.com/login" rel="noopener noreferrer">https://accounts.google.com/login</a>)</li>
<li>Username of the account</li>
<li>Password of the account</li>
<li>QR code image from Google Authenticator or text file from Chrome Authenticator extension.</li>
</ol>
<p>The last item is optional. If you do not have a QR code image or text file, you can skip this step. You can add the MFA token later. or use witout MFA.</p>
<h3>How To</h3>
<p>Before using the <code>aws-keychain</code> command, you need to register an AWS account. You can do this by running the following command:</p>
<pre style="background-color:#263238;"><span style="color:#82aaff;">aws-keychain register</span><span style="color:#89ddff;"> --</span><span style="color:#f78c6c;">qr-path </span><span style="color:#89ddff;">&lt;</span><span style="color:#82aaff;">path</span><span style="color:#89ddff;">&gt; -</span><span style="color:#82aaff;">-txt-path </span><span style="color:#89ddff;">&lt;</span><span style="color:#82aaff;">path</span><span style="color:#89ddff;">&gt;
</span></pre>

<p>where <code>--qr-path</code> is the path to specify the QR code image from Google Authenticator and <code>--txt-path</code> is the path to specify the text file from Chrome Authenticator extension.</p>
<p>After reading the QR code or text file, the interactive prompt will ask you to enter required information to register the account.</p>
<pre style="background-color:#263238;"><span style="color:#82aaff;">aws-keychain register</span><span style="color:#89ddff;"> --</span><span style="color:#f78c6c;">qr-path
</span><span style="color:#82aaff;">Setting up the keychain for the account XXXXXXXXXXXXX (Amazon Web Services</span><span style="color:#eeffff;">)
</span><span style="color:#82aaff;">Enter the URL of the account (e.g. https://accounts.google.com/login</span><span style="color:#eeffff;">)</span><span style="color:#82aaff;">: https://XXXXXXXXXXX.signin.aws.amazon.com/console
</span><span style="color:#82aaff;">Enter the username of the account: my-username
</span><span style="color:#82aaff;">Enter the password of the account: my-password
</span><span style="color:#82aaff;">Enter the name for the keychain entry: staging
</span></pre>

<p>The value <code>stagin</code> is the name of the keychain entry. It is used to choose the account when logging in.</p>

  

        </main>
      </div>

      <footer>
        
          <a href="https://github.com/acn-gen-tomita/binary-zone"><div class="github-icon" aria-hidden="true"></div></a>
        
        <span>
          aws-keychain, MIT
        </span>
      </footer>
    </div>

    
    

    
  </body>
</html>