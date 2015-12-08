
# Install

cat https://raw.githubusercontent.com/cschneider/Karaf-Tutorial/master/tasklist-blueprint-cdi/org.ops4j.datasource-tasklist.cfg | tac -f etc/org.ops4j.datasource-tasklist.cfg
feature:repo-add pax-jdbc 0.7.0
feature:install pax-jdbc-h2 pax-jdbc-pool-dbcp2 pax-jdbc-config jpa hibernate transaction http-whiteboard
install -s mvn:net.lr.example.jpa/tasklist-blueprint/1.0.0-SNAPSHOT
