################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/USB/subdir.mk
-include src/PERIPHERAL/subdir.mk
-include src/OTHER/subdir.mk
-include src/MODE/subdir.mk
-include src/MAIN/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: RT-BT-9AXIS-sample.axf

# Tool invocations
RT-BT-9AXIS-sample.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\ryota\OneDrive\RT working\RT-BT-9AXIS-00\lpcXpresso\workspace\CMSISv1p30_LPC13xx\Debug" -Xlinker -Map="RT-BT-9AXIS-sample.map" -Xlinker --gc-sections -mcpu=cortex-m3 -mthumb -T "RT-BLUETOOTH-9AXIS-sample_Debug.ld" -o "RT-BT-9AXIS-sample.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) RT-BT-9AXIS-sample.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "RT-BT-9AXIS-sample.axf" ; arm-none-eabi-objcopy -v -O binary "RT-BT-9AXIS-sample.axf" "RT-BT-9AXIS-sample.bin" ; checksum -p LPC1343 -d "RT-BT-9AXIS-sample.bin"
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
