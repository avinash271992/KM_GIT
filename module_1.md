#include<linux/fs.h>
#include<linux/kernel.h>
#include<linux/module.h>
#include<linux.init.h>
static int first_program()
{
printk("Inside your first module\n");
return 0;
}
static void first_program_exit()
{
printk("exiting from your first module\n");
}
module_init(first_program);
module_exit(first_program_exit);
