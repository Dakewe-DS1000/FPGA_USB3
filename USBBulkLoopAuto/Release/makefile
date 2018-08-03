################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: USBBulkLoopAuto.elf secondary-outputs

# Tool invocations
USBBulkLoopAuto.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: Cross ARM C Linker'
	/Users/yuqiyue/Documents/FX3_SDK_1.3.4_MacOS/yagarto-4.7.2/bin/arm-none-eabi-gcc -mcpu=arm926ej-s -marm -mthumb-interwork -O3 -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall  -g -T "/Users/yuqiyue/Documents/FX3_SDK_1.3.4_MacOS/cyfx3sdk/fw_build/fx3_fw/fx3.ld" -nostartfiles -Xlinker --gc-sections -L"/Users/yuqiyue/Documents/FX3_SDK_1.3.4_MacOS/cyfx3sdk/fw_lib/1_3_4/fx3_release" -Wl,-Map,"USBBulkLoopAuto.map" -Wl,-d -Wl,--no-wchar-size-warning -Wl,--entry,CyU3PFirmwareEntry -o "USBBulkLoopAuto.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(ASM_DEPS)$(S_UPPER_DEPS) USBBulkLoopAuto.elf
	-@echo ' '

post-build:
	-@echo 'Generate boot-loadable firmware binary'
	-/Users/yuqiyue/Documents/FX3_SDK_1.3.4_MacOS/cyfx3sdk/util/elf2img/elf2img -i USBBulkLoopAuto.elf -o USBBulkLoopAuto.img -v
	-@echo ' '

secondary-outputs:

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
