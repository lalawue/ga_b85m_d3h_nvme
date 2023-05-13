
英文翻译自 baidu | English traslated by https://fanyi.baidu.com/#auto/zh/ with little modification

# GA-B85M-D3H 主板支持 NVME 系统盘

大概流程如下

- 找一个安装了 Win10 的 SSD 启动到系统
- 安装最新的 @BIOS 软件
- 使用 @BIOS 读取并备份主板的 BIOS 到 bios.bin
- 使用 MMTool 在 Win10/Win11 编辑 bios.bin（记得先备份）
- 找到并删除 MOemLogo、MyOemLogo1、MyOemLogo2 这 3 个模块
- 找到 CSMCORE 后，点击插入 NvmExpressDxe_Small.ffs，选中压缩插入 
- 使用 @BIOS 刷入刚保存好的 bios.bin
- 将 NVME 盘接上 PICE 转接卡接入到 PCIEx4 的插槽中
- 重启按 DEL 进入到 BIOS，可以看到 PATA SS: 盘，可以作为系统盘


# GA-B85M-D3H motherboard supports NVME system disks

The general process is as follows

- Find an SSD with Win10 installed to boot to the system
- Install the latest @BIOS software
- Use @BIOS to read and backup the motherboard's BIOS to bios.bin
- Using MMTool to edit bios.bin in Win10/Win11 (remember to backup first)
- Find and delete the MOemLogo, MyOemLogo1, and MyOemLogo2 modules
- After finding CSMCORE, click to insert NvmExpressDxe_Small.ffs, selected for compression insertion
- Use @BIOS to brush in the newly saved bios.bin
- put NVME disk with PICE adapter into the slot of PCIEx4
- Restart and press DEL to enter the BIOS. You can see the PATA SS: disk, which can be used as the system disk
