# ✅ FxUAV Network Manager – Development Checklist

## 📍 Phase 1: Planning & Requirements
- [x] Finalize scope (exclude video stream metrics for now)
- [x] Choose GUI stack (PyGObject/GTK or PyQt)
- [x] Freeze tech stack (Python, mmcli, nmcli, speedify_cli)
- [x] Finalize target hardware (RPi, Jetson Nano/Orin)
- [x] Refine GUI wireframe

---

## 🧱 Phase 2: Project Setup
- [x] Initialize project directory and folders
- [x] Set up `.gitignore` and `README.md`
- [ ] Set up `requirements.txt` and virtual environment
- [ ] Write basic `config.yaml` schema (APNs, Speedify credentials)
- [ ] Create architecture diagram or doc

---

## 🧪 Phase 3: Backend Modules
- [ ] `modem_manager.py`: USB, mmcli, SIM, signal, registration
- [ ] `nmcli_wrapper.py`: Add/edit/delete GSM profiles
- [ ] `speedify_wrapper.py`: Start, monitor bonding, gather stats
- [ ] `watchdog.py`: Monitor Speedify daemon health
- [ ] Logging system (`logs/fxuav-net.log`)

---

## 🖼️ Phase 4: GUI Development
- [ ] Build layout (Tabs: Modem, Connections, Bonding, Logs)
- [ ] Display real-time modem + SIM + signal status
- [ ] Implement APN profile management
- [ ] Embed bonding stats into GUI
- [ ] Add action buttons: connect, delete, reset modem, bonding toggle

---

## 🧪 Phase 5: Testing
- [ ] Unit test backend modules
- [ ] Full flow test on RPi/Jetson (boot → bond)
- [ ] Simulate modem disconnection
- [ ] Kill Speedify daemon and test recovery
- [ ] Verify bonding health under weak signal

---

## 🚀 Phase 6: Packaging & Deployment
- [ ] Create `.deb` package or install script
- [ ] Setup autostart (systemd optional)
- [ ] Store configs in `/etc/fxuav-net/`
- [ ] Pin Speedify version

---

## 📚 Phase 7: Documentation
- [ ] Developer README (architecture, modules)
- [ ] User Manual (GUI usage, modem + bonding)
- [ ] Known issues / FAQ
- [ ] Error Code Reference Sheet

---

## 🔁 Phase 8: Future Features
- [ ] Add Video Stream Metrics Module
- [ ] SIM hotplug detection
- [ ] GPS status panel
- [ ] Remote dashboard sync
