################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
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
Project\ -\ 1\ -\ BlinkyTest.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Project\ -\ 1\ -\ BlinkyTest.list \

OBJCOPY_BIN += \
Project\ -\ 1\ -\ BlinkyTest.bin \


# All Target
all: Project\ -\ 1\ -\ BlinkyTest.elf secondary-outputs

# Tool invocations
Project\ -\ 1\ -\ BlinkyTest.elf: $(OBJS) $(USER_OBJS) D:\temp\CileGomuluSistemEgitimi\STM32CubeIDE\Project\ -\ 1\ -\ BlinkyTest\STM32F070RBTX_FLASH.ld
	arm-none-eabi-gcc -o "Project - 1 - BlinkyTest.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"D:\temp\CileGomuluSistemEgitimi\STM32CubeIDE\Project - 1 - BlinkyTest\STM32F070RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Project - 1 - BlinkyTest.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Project\ -\ 1\ -\ BlinkyTest.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Project - 1 - BlinkyTest.list"
	@echo 'Finished building: $@'
	@echo ' '

Project\ -\ 1\ -\ BlinkyTest.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Project - 1 - BlinkyTest.bin"
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
