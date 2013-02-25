Casio VX-100 SDK for Appcelerator Titanium
==========================================

    var casiosdk = require('id.web.ravintola.casiosdk');

    function cdChangeColor(e) {
      // 1 = Green , 2 = Emerald Green , 3 = White , 0 = Off
      casiosdk.lineDisplaySetBackground(e.source.color);
    }

    // Eject cash drawer
    casiosdk.drawerEject();
    
    // Read Magnetic Card
    // obj will return object with 3 key {track1: "" , track2: "" , track3: ""}
    var obj = casiosdk.mcrRead();
    
    // Print to com port
    // comport = 1 / 2
    // baud = normally 9600 for TMU-220 , 19200 for TMT-81
    casiosdk.printComPort(comPort , baud , strintToPrint);
    
    // Line Display
    // line1 and line2 20 byte string. Excess string will be truncated
    casiosdk.lineDisplay(line1 , line2);
    
    // Print to build in printer
    casiosdk.printText(value);
