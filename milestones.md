# Malware Dev / RE Learning Roadmap

## Stage 1 — Finish the Keylogger (current)
- [ ] Daemonize with `fork()` + `setsid()`
- [ ] Signal handler for clean shutdown (`SIGINT`)

---

## Stage 2 — Linux Internals
- [ ] Write a basic shell (`fork`, `execve`, `waitpid`, pipes)
- [ ] Write a basic strace clone using `ptrace()`

---

## Stage 3 — Networking
- [ ] Finish C2 server in C
- [ ] Add a reverse shell (client connects back to C2)
- [ ] Raw sockets — craft packets manually

---

## Stage 4 — Userland Stealth
- [ ] LD_PRELOAD rootkit — hide process from `ps`, hide logfile from `ls`
- [ ] Process hollowing / ptrace injection in C
- [ ] **Defensive:** write a detector for LD_PRELOAD rootkits

---

## Stage 5 — Kernel Space
- [ ] Hello world LKM (kernel module)
- [ ] Syscall hook from kernel space
- [ ] Hide a process from `/proc` at kernel level
- [ ] **Defensive:** LKM that detects hooked syscall table entries

---

## Ongoing — Reverse Engineering (parallel habit)
- [ ] After every project: RE with symbols (`objdump`, `gdb`)
- [ ] Then strip symbols, RE again
- [ ] Then compile with `-O2`, RE again

---

## End Goal
Be able to analyze real unknown binaries and understand malware at the kernel level.
