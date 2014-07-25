WD=.
DIST=$(WD)/dist
TGZ=ref-app.tar.gz

usage:
	# This Makefile used to generate distributables. See contents to figure out usage.

make-dist: package prepare-dist zip-dist

package:
	mvn $(opts) clean package

prepare-dist:
	rm -fr $(DIST)
	mkdir $(DIST) 
	cp -a $(WD)/config $(DIST)/
	cp -a $(WD)/*.sh $(DIST)/
	mkdir -p $(DIST)/target
	cp -a $(WD)/target/classes $(DIST)/target/
	cp -a $(WD)/target/dependency $(DIST)/target/

zip-dist:
	tar czf $(TGZ) $(DIST)

