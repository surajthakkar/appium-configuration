# appium-configuration

Important setup notes
================= 
-> Be an admin on your Windows/Mac
-> Use latest Windows/MacOS operating system
-> Office machine? make sure anti-virus and company policies are not blocking installation of Appium and associated softwares
-> If practicing using an Android emulator, use a powerful processor and sufficient RAM
-> Avoid using phone from Chinese manufacturers that may restrict Appium due to their security limitations


Install homebrew [package manager for macOS and is used to install software packages]
======================================================================================
Link: https://brew.sh/
Command: /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"


Install node and npm [Appium dependencies]
===============================================
Commands to check if node and npm are installed:
node -v
npm -v
Command to install node: brew install node [This will install npm as well]
Command to check node installation path: where node or which node


Install Appium CLI server
=========================
-> Command to install Appium using npm: npm install -g appium@next
Note: @next will not be required once Appium 2.0 stable release is out to market.
-> Command to install specific version: npm install -g appium@<verion_number>
-> Command to start Appium: appium
-> Command to get installation location: where appium
Note: This command only gives location of the shortcut, not the actual installation location.
Actual installation location is this: /usr/local/lib/node_modules/appium
-> Command to uninstall Appium: npm uninstall -g appium


Install Appium Inspector
========================
-> Download and install from https://github.com/appium/appium-inspector/releases


Install JAVA JDK (not the JRE!)
================================
-> Command to check if JAVA is already installed: java -version
-> JAVA JDK download link: https://www.oracle.com/technetwork/java/javase/downloads/index.html
Important note: Please use Java 8/11/15 for now. Don't use Java 16 or higher. The current Appium Java Client 8.x.x is not compatible with Java 16+. You may use Java 16+ once Appium Java client becomes compatible.


Set JAVA_HOME environment variable
==================================
On macOS 10.15 Catalina and later, default shell is zsh: 
--------------------------------------------------------
-> Navigate to home directory: cd ~/
-> Open zshrc file: open -e .zshrc
-> Create zshrc file: touch .zshrc
-> Add below entries:
export JAVA_HOME=$(/usr/libexec/java_home)
export PATH="${JAVA_HOME}/bin:${PATH}"
-> source .zshrc
-> echo $JAVA_HOME
-> echo $PATH
Follow this article: https://mkyong.com/java/how-to-set-java_home-environment-variable-on-mac-os-x/

