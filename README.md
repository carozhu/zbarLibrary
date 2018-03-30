# zbarLibrary

```
compile 'com.carozhu:zbarLibrary:1.0.0'
```

> scan qrcode for enter. just such as :

``` java
      net.sourceforge.zbar.Image barcode = new net.sourceforge.zbar.Image(width, height, "Y800");
                    barcode.setData(data);
                    int result = scanner.scanImage(barcode);
                    //have checked qrcode enter.
                    if (result > 0) {
                       // TODO: ScanDecodeResultBlurryCallback()

                    }
                    //have checked right qrcode.
                    if ((result - 1) != 0) {
                        SymbolSet syms = scanner.getResults();
                        String scanReuslt = null;
                        for (Symbol sym : syms) {
                            String tempScanReuslt = sym.getData();
                            if (!TextUtils.isEmpty(tempScanReuslt)) {
                                scanReuslt = tempScanReuslt;
                                Log.i(TAG, "barcode result " + tempScanReuslt);
                            }
                        }
                        if (!TextUtils.isEmpty(scanReuslt)) {
                            //TODO: ScanDecodeResultOkCallback(scanReuslt);
                        }
                    }
```


