################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
L432KC_Blinking_Led.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
L432KC_Blinking_Led.list \

OBJCOPY_BIN += \
L432KC_Blinking_Led.bin \


# All Target
all: L432KC_Blinking_Led.elf secondary-outputs

# Tool invocations
L432KC_Blinking_Led.elf: $(OBJS) $(USER_OBJS) /home/steamhyperpolyglot/RnD/STM32-dev/L432KC_Blinking_Led/STM32L432KCUX_FLASH.ld
	arm-none-eabi-gcc -o "L432KC_Blinking_Led.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/steamhyperpolyglot/RnD/STM32-dev/L432KC_Blinking_Led/STM32L432KCUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="L432KC_Blinking_Led.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

L432KC_Blinking_Led.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "L432KC_Blinking_Led.list"
	@echo 'Finished building: $@'
	@echo ' '

L432KC_Blinking_Led.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "L432KC_Blinking_Led.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
