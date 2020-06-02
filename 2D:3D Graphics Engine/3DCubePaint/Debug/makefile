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
all: 3DCubePaint.axf

# Tool invocations
3DCubePaint.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"/Users/akanshajajodia/Documents/MCUXpressoIDE_11.1.1/workspace/CMSIS_CORE_LPC17xx/Debug" -Xlinker -Map="3DCubePaint.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "DrawLine_Debug.ld" -o "3DCubePaint.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) 3DCubePaint.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "3DCubePaint.axf"; # arm-none-eabi-objcopy -v -O binary "3DCubePaint.axf" "3DCubePaint.bin" ; # checksum -p LPC1769 -d "3DCubePaint.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
