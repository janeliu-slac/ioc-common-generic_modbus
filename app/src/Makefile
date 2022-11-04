TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build an ioc application
# Use PROD_IOC_RTEMS for RTEMS only
# Use PROD_IOC_Linux for Linux only
PROD_IOC_Linux = gmb

# gmb.dbd will be created and installed
DBD += gmb.dbd

gmb_DBD += base.dbd
gmb_DBD += iocAdmin.dbd
gmb_DBD += asSupport.dbd
gmb_DBD += asyn.dbd
gmb_DBD += modbus.dbd
gmb_DBD += modbusSupport.dbd
gmb_DBD += caPutLog.dbd

# <name>_registerRecordDeviceDriver.cpp will be created from <name>.dbd
gmb_SRCS += gmb_registerRecordDeviceDriver.cpp
gmb_SRCS_DEFAULT += gmbMain.cpp

# Add locally compiled object code
#gmb_SRCS += dbSubExample.c

gmb_LIBS += autosave
gmb_LIBS += devIocStats
gmb_LIBS += modbus
gmb_LIBS += caPutLog
gmb_LIBS += asyn
gmb_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

