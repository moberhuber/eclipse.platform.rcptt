# eclipse.platform.rcptt-tests
RCPTT Tests for Eclipse Platform and SDK (JDT, PDE) functionality.
For full RCPTT docs see https://www.eclipse.org/rcptt/

Run with Maven
==============
1. Symlink or copy your Eclipse install to test into (gitroot)/aut/eclipse
   Or, edit JavaSDKTests/pom.xml/<aut><explicit> tag to point to your Eclipse
2. mvn clean package  ## will download/build 360 MiB

Run with RCPTT Standalone SDK
=============================
1. Download and extract RCPTT (note: 2.2.0-milestone is needed for Oxygen!)
   http://download.eclipse.org/rcptt/milestone/2.2.0/M6/ide/?d
2. Launch RCPTT, pick a workspace.
3. In the "Applications" view on bottom, add your Eclipse path
4. File > Import > General : Existing Projects into Workspace > JavaSDKTests
5. Right-click > Run As > Test Cases

Run with RCPTT plug-in from source workspace
============================================
1. Help > Install New Software, use URL:
   http://download.eclipse.org/rcptt/nightly/2.2.0/latest/full/repository
   install "RCPTT IDE" and restart
2. File > Import > General : Existing Projects into Workspace > JavaSDKTests
3. Right-click > Run As > Test Cases
   It should find the "SDKTests" Launch automatically for launching your
   workspace against the current target platform.

Known Limitations
=================
* The pom.xml for Maven is not really polished, it's basically generated
  as-is from RCPTT standalone.
* The self-hosted launch from source is not as stable as launching against
  an explicit target platform (RCPTT IDE dependencies may interfere with 
  the application). Launching from Maven or standalone is much more stable.

License
=======
<pre>
    Copyright (c) 2009, 2016 Xored Software Inc and others.
    All rights reserved. This program and the accompanying materials
    are made available under the terms of the Eclipse Public License v1.0
    which accompanies this distribution, and is available at
    http://www.eclipse.org/legal/epl-v10.html
     
    Contributors:
    	Xored Software Inc - materials generated by RCPTT
        Martin Oberhuber - JavaSDKTest and this README
</pre>

