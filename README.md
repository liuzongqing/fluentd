fluentd
=======

yum install td-agent on centos(required libyaml td-libyaml)

cat >/etc/yum.repos.d/td.repo <<'EOF';
[treasuredata]
name=TreasureData
baseurl=http://packages.treasuredata.com/redhat/\$basearch
gpgcheck=1
gpgkey=http://packages.treasuredata.com/GPG-KEY-td-agent
EOF

yum install td-agent

=======

for fluentd(td-agent)

export GEM_HOME="/usr/lib64/fluent/ruby/lib/ruby/gems/1.9.1/"

export GEM_PATH="/usr/lib64/fluent/ruby/lib/ruby/gems/1.9.1/"

/usr/lib64/fluent/ruby/bin/fluent-gem sources --add http://rubygems.org/

=======
type rawexec

/usr/lib64/fluent/ruby/bin/fluent-gem install fluent-plugin-rawexec

/usr/lib64/fluent/ruby/bin/fluent-gem install fluent-plugin-rawexec


=======
type multiprocess

/usr/lib64/fluent/ruby/bin/fluent-gem install fluent-plugin-multiprocess

http://docs.fluentd.org/articles/in_multiprocess

=======
type s3

/usr/lib64/fluent/ruby/bin/fluent-gem install fluent-funplus-s3


