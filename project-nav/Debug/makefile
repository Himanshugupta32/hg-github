################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
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
all: project-nav.axf

# Tool invocations
project-nav.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/home/studentadmin/Documents/MCUXpresso_10.3.0_2200/workspace/lpc_board_nxp_lpcxpresso_1769/Debug" -L"/home/studentadmin/Documents/MCUXpresso_10.3.0_2200/workspace/lpc_chip_175x_6x/Debug" -Xlinker -Map="project-nav.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "project-nav_Debug.ld" -o "project-nav.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) project-nav.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "project-nav.axf"; # arm-none-eabi-objcopy -v -O binary "project-nav.axf" "project-nav.bin" ; # checksum -p LPC1769 -d "project-nav.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
