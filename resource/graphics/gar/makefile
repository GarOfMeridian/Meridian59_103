# Makefile 

TOPDIR=..\..\..
!include $(TOPDIR)\common.mak

SOURCEDIR = .

BGFS = ilink.bgf

all:
	@-for %i in ($(BGFS)) do \
   	@$(CP) %i $(CLIENTRUNDIR)\resource >nul
	@-for %i in ($(DIRS)) do \
		@if EXIST %i (	cd %i & \
      @echo Make in %i & \
	 	$(MAKE) /$(MAKEFLAGS) $(COMMAND) &\
		cd .. )

clean:
	@-for %i in ($(DIRS)) do \
		@echo Making clean in %i & \
		@if EXIST %i ( cd %i & \
	 	$(MAKE) /$(MAKEFLAGS) clean &\
		cd .. )
