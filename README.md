# password-validator
nodejs and rust
====================================================================

HOW TO RUN: PASSWORD VALIDATOR (NODE.JS & RUST)

====================================================================

Project Root: C:\Users\gamer\Desktop\all stupid project\password-validator



--------------------------------------------------------------------

1. RUN JAVASCRIPT (NODE.JS) VERSION

--------------------------------------------------------------------

1. Navigate to the JS folder:

   cd js-version



2. Run the program:

   node index.js



[Troubleshooting JS]

- If you see "ERR_INVALID_PACKAGE_CONFIG":

  del package.json

  node index.js



--------------------------------------------------------------------

2. RUN RUST VERSION

--------------------------------------------------------------------

1. Navigate to the Rust folder:

   cd rust-version



2. Compile and run the program:

   cargo run



[Troubleshooting Rust]

- If PowerShell says "'cargo' is not recognized":

  $env:Path += ";$env:USERPROFILE\.cargo\bin"

  cargo run

  (Tip: Restart your PC once to make this permanent.)



- If you see "linker 'link.exe' not found":

  rustup toolchain install stable-x86_64-pc-windows-gnu

  rustup default stable-x86_64-pc-windows-gnu

  cargo run



--------------------------------------------------------------------

3. SWITCHING BETWEEN FOLDERS IN TERMINAL

--------------------------------------------------------------------

- From js-version to rust-version:

  cd ..\rust-version



- From rust-version to js-version:

  cd ..\js-version



--------------------------------------------------------------------

4. TEST CASES (OWASP ASSIGNMENT REQUIREMENTS)

--------------------------------------------------------------------

- FAIL (Too short - 14 chars):

  12345678901234



- PASS (Leading/trailing spaces preserved - 15 chars total):

     123456789012



- PASS (No uppercase/numbers/symbols required - 15+ chars):

  thisisjustalonglowercasepassword



- PASS (Unicode & 64+ characters):

  รหัสผ่านภาษาไทยและอีโมจิ🔒🔑ที่ยาวเกินหกสิบสี่ตัวอักษรเพื่อทดสอบระบบตรวจสอบความปลอดภัยของรหัสผ่าน
