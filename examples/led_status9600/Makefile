PROGRAM = led_status

EXTRA_COMPONENTS = \
	extras/http-parser \
	$(abspath ../../components/common/wolfssl) \
	$(abspath ../../components/common/cJSON) \
	$(abspath ../../components/common/homekit) \
	$(abspath ../../components/esp-8266/led-status)

FLASH_SIZE ?= 32

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS

include $(SDK_PATH)/common.mk

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 9600 --elf $(PROGRAM_OUT)
