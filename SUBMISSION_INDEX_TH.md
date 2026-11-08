# ชุดส่งงาน RAE67 Labs 02–07

**ชื่อ:** ณัฐพงษ์ มาดชาย  
**รหัส:** 6752500231  
**กลุ่ม:** สาธุ  
**วันที่:** 8 พฤศจิกายน 2569

ชุดนี้แยกตามโฟลเดอร์ `lab_02` ถึง `lab_07` โดยมี source ที่ตรวจแล้ว, รายงานพร้อมชื่อผู้จัดทำ, ผลรัน/CSV/config/manifest และใบงาน Word ที่กรอกแล้วสำหรับ Lab 04–07 ดู source tree เพิ่มเติมได้จาก `RAE67_bio_ins-main.zip`

## สถานะ

- Lab 02: controller grader ผ่าน 10/10; student C0–C3 comparison มี 20 trials, C2 robustness short/full มี 15/45 trials; แนบกราฟ C1 SVG และ C2 PNG
- Lab 03: CPG grader ผ่าน 5/5; gait comparison baseline/fast/high_gain และ Week 04 bridge CSV/contract พร้อมรายงาน
- Lab 04: code checker ผ่าน 13/13 และมี comparison กับ extreme-test artifacts
- Lab 05: worksheet/report และ comparison, one-factor, fault, contact mini-lab results ครบ
- Lab 06: policy ผ่าน baseline/group contract 40/40 และมี paired C0/C1 กับ replay byte-identical
- Lab 07: policy/proposal checkers ผ่าน; offline paired trials, replay และ ROS 2 Jazzy WSL build/three-process smoke run แนบแล้ว

Lab 02 unit tests มี 2 ข้อที่ออกแบบให้ตรวจว่า starter ที่ยังไม่เสร็จต้อง fail; เมื่อใช้ controller ที่ implement ครบ ข้อ starter-only เหล่านี้จึง fail ตามเงื่อนไขเดิม แต่ `grade_submission.py` ผ่าน 10/10 checks

`RAE67_bio_ins-main.zip` บรรจุ source, manuals, configs และ code ของโฟลเดอร์หลัก โดยไม่รวม `.venv`, `__pycache__`, `*.pyc`, generated `results/` และ ZIP submission ซ้ำ; ผลทดลองทั้งหมดอยู่ใน `RAE67_Labs_02-07_Submission.zip`

## ข้อจำกัดที่ยังเปิดเผยไว้

Lab 07 ROS trace มี input receive counts ต่ำกว่า publish counts เล็กน้อยและ collector ขาด records ตอนท้าย จึงยังไม่สรุปว่า delivery ครบหรือทราบต้นเหตุ; รายละเอียดอยู่ใน `lab_07/Lab07_ROS2_Run_Report_TH.md` และ raw traces ใน `lab_07/results/copilot_ros_run02/`. ยังไม่มี AHM–CPG integration trial เต็มรูปแบบ, physical robot calibration, hardware motion/RGB latency หรือ human-participant trial