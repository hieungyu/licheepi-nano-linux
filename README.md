
# How to build a Linux System on LicheePi Nano
### Link:
- https://drive.google.com/file/d/1vLvuNA93Iibmg85RVmE3XCrYvlGcCqmO/view

**Custom Embedded Linux System for LicheePi Nano (F1C100s)**

- Built from scratch using Buildroot
- Custom boot flow: BROM → SPL → U-Boot → Kernel → RootFS
- Containerized build environment using Docker

### Why use Docker in  this Project ? 
I think it will be cool and learn new somethings. Besides, I want to a see about CI/CD in Production, it help me more knowleaged 😁😂

So I decided to use Docker Containers instead of setting up a traditional Linux Virtual Machine (VM) or Linux native. This decision aimed to create a completely isolated cross-compilation environment, thoroughly addressing the risk of library conflicts between computers, and also served as a necessary foundation for automating continuous integration/compilation (CI/CD) processes according to modern industry standards.

### Run container:

```bash
docker run -it --rm lichee_build_env
```

- **Note**:
1. ```-it``` : open terminal
2. ```--rm``` : when exit container, it'll clean container .


## Key Learnings

- Deep understanding of embedded Linux boot flow
- Experience debugging kernel boot issues via UART
- Ability to build reproducible environments using Docker

### Docs: 
- https://fanning.vn/study_licheepinano/nano_buildsystem.html
- Boot flow: https://labs.dese.iisc.ac.in/embeddedlab/device-tree-and-boot-flow/