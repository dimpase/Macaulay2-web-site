all signature: setup.ini.sig
setup.ini: Macaulay2/* Macaulay2-icons/* 
	genini --okmissing=source Macaulay2 Macaulay2-icons >setup.ini.tmp
	mv setup.ini.tmp setup.ini
setup.ini.sig: setup.ini
	rm -f "$@"
	gpg --detach-sign --local-user "Macaulay2" setup.ini
clean:; rm -f setup.ini setup.ini.sig
distclean:; rm -f Makefile Macaulay2-icons/server.hint
