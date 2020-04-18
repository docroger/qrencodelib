# qrencodelib
qrcode library for QRCODE creation, coded by FUKUCHI. Compiled DLL and lib files.

For Purbasic usage :

ImportC "d:\perso\qrencodelib.lib" ; change the path for your lib
  CompilerIf #PB_Compiler_Processor=#PB_Processor_x86
  QRcode_encodeString8bit(Text.p-ascii, Version.l, QRecLevel.l) As "_QRcode_encodeString8bit"
  QRcode_free(*Qrcode.QRCode) As "_QRcode_free"
  CompilerElse
  QRcode_encodeString8bit(Text.p-ascii, Version.l, QRecLevel.l) As "QRcode_encodeString8bit"
  QRcode_free(*Qrcode.QRCode) As "QRcode_free"
  CompilerEndIf
EndImport
