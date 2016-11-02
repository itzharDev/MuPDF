Compiled MuPDF for android

right now for armeabi armeabi-v7a mips

min API 14


last compiled - 11/2/2016


usage:


settings.gradle:

    include ':mupdf'
    project(':mupdf').projectDir = new File('../../../Desktop/mupdf/platform/android/viewer')


build.gradle:

    dependencies {
        compile project(':mupdf')
    }


Java:
    //file provider from skd 25 - otherwise use old method to get file Uri
    
    Uri contentUri = FileProvider.getUriForFile(context, context.getApplicationContext().getPackageName() + ".provider", filePath);
    Intent intent = new Intent(context, MuPDFActivity.class);
    intent.setAction(Intent.ACTION_VIEW);
    intent.setData(contentUri);
    startActivity(intent);
