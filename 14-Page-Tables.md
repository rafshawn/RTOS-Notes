```TODO: FINISH THIS CHAPTER```
# Paging in Practice:
Dominant model for virtual memory

# 32b Intel Page Table Entry
- R/W bit enables writing to page
- U/S bit marks page supervisor-access-only
- A bit indicates page accessed recently
- D bit shows page modified recently

# 64b Intel Page Table Entry:
- Bigger virtual address with extensibility
- XD (eXecute Disable) for security

# Page Table Size:
- Describes 32b of virtual and physical memory with 4 kiB pages

# Page Tables in Practice:
- Multi-level page tables create trees of pages

# Superpages in x86-64:
- Utilize up to 2 MiB pages.

# Super-duper-pages in x86-64:
- Supports up to 1 GiB pages