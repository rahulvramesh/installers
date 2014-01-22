#Create rpm for wget enter command

<code>wget http://ftp.gnu.org/gnu/wget/wget-1.15.tar.gz -P ~/rpmbuild/SOURCES/</code>

<code>cd ~/rpmbuild/SPECS/</code>

<code>wget https://github.com/zpanel/installers/raw/master/install/CentOS-6_4/compile/wget/wget.spec</code>

<code>rpmbuild -ba wget.spec</code>

#Regenerate repo

<code>cd ~/rpmbuild/RPMS/$(uname -m)</code>

<code>createrepo --update ./</code>

#Install (just update lol)

<code>yum -y update</code>
