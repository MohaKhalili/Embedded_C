################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
000TestProject.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
000TestProject.list \

OBJCOPY_BIN += \
000TestProject.bin \


# All Target
all: 000TestProject.elf secondary-outputs

# Tool invocations
000TestProject.elf: $(OBJS) $(USER_OBJS) D:\Engineering\ Training\ Files\4-Embedded\ system\0-STM\1-Learning\0-videos\0\ -\ Udemy\Microcontroller\ Embedded\ C\ Programming\ absolute\ beginners\ 2020-2\0_Workstation\Embedded_C\target\000TestProject\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "000TestProject.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Engineering Training Files\4-Embedded system\0-STM\1-Learning\0-videos\0 - Udemy\Microcontroller Embedded C Programming absolute beginners 2020-2\0_Workstation\Embedded_C\target\000TestProject\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="000TestProject.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

000TestProject.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "000TestProject.list"
	@echo 'Finished building: $@'
	@echo ' '

000TestProject.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "000TestProject.bin"
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
