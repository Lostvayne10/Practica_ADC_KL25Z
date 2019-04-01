################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include utilities/subdir.mk
-include startup/subdir.mk
-include source/subdir.mk
-include drivers/subdir.mk
-include board/subdir.mk
-include CMSIS/subdir.mk
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
all: FotoResistencia\ project_driver_examples_adc16_polling.axf

# Tool invocations
FotoResistencia\ project_driver_examples_adc16_polling.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -Xlinker -Map="FotoResistencia project_driver_examples_adc16_polling.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -Xlinker --sort-section=alignment -mcpu=cortex-m0plus -mthumb -T FotoResistencia_project_driver_examples_adc16_polling_Debug.ld -o "FotoResistencia project_driver_examples_adc16_polling.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) "FotoResistencia project_driver_examples_adc16_polling.axf"
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "FotoResistencia project_driver_examples_adc16_polling.axf"; # arm-none-eabi-objcopy -v -O binary "FotoResistencia project_driver_examples_adc16_polling.axf" "FotoResistencia project_driver_examples_adc16_polling.bin" ; # checksum -p MKL25Z128xxx4 -d "FotoResistencia project_driver_examples_adc16_polling.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
