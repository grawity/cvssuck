all: cvssuck.png

clean:
	rm -f cvssuck.png cvssuck.ppm cvssuck.ps

cvssuck.png: cvssuck.ppm
	pnmtopng cvssuck.ppm > cvssuck.png 

cvssuck.ppm: cvssuck.ps
	gs -q -dNOPAUSE \
	  -sDEVICE=ppmraw -sOutputFile=cvssuck.ppm \
	  -dGraphicsAlphaBits=4 -g300x90 \
	  -c -90 -650 translate -- \
	  cvssuck.ps quit.ps 

cvssuck.ps: cvssuck.sk
	sk2ps cvssuck.sk > cvssuck.ps
