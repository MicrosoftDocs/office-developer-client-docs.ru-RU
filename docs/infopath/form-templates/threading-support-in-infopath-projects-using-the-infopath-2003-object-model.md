---
title: Поддержка потоков в проектах InfoPath, использующих объектную модель InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- multithreading [infopath 2007], infopath 2003-compatible form templates,threading [InfoPath 2007], support for projects using InfoPath 2003 object model,InfoPath 2003-compatible form templates, threading support
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: COM-объекты, доступ к которым предоставляется через сборки взаимодействия Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll и Microsoft.Office.Interop.InfoPath.Xml.dll, установленные приложением Microsoft InfoPath, не поддерживают вызовы в нескольких потоках. В число таковых входят интерфейсы MSXML, реализуемые пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust (в именах большинства которых используется префикс IXMLDOM), а также все интерфейсы, предоставляемые пространством имен Microsoft.Office.Interop.InfoPath.Xml, которые не обеспечивают точную синхронизацию потоков.
ms.openlocfilehash: ca00593eebe17586c4f77b4b91adc158c4f649fd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537845"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>Поддержка потоков в проектах InfoPath, использующих объектную модель InfoPath 2003

COM-объекты, доступ к которым предоставляется через сборки взаимодействия Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll и Microsoft.Office.Interop.InfoPath.Xml.dll, установленные приложением Microsoft InfoPath, не поддерживают вызовы в нескольких потоках. Это включает интерфейсы для объектов MSXML (MSXML), которые завернуты пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust** (большинство из которых имеют имена, префикс которых с IXMLDOM) [](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) и все интерфейсы, открытые пространством именMicrosoft.Office.Interop.InfoPath.Xml, ни один из которых не является безопасным для потоков. 
  
Все вызовы этих COM-объектов необходимо выполнять в одном потоке. Управляемый код в проекте InfoPath может создавать другие потоки для фоновой работы, но вызовы объектной модели может осуществлять только главный поток.
  
Если в проекте InfoPath с управляемым кодом используется несколько потоков, то следует осторожно распределять объекты между потоками. Нельзя распределять между потоками ссылки на модель XML DOM и ссылки на объекты InfoPath. 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>Осуществление асинхронных вызовов объектной модели InfoPath

В случаях, когда необходимо вызвать процесс, например таймер, запущенный в отдельном потоке, можно проигнорировать тот факт, что объектная модель InfoPath не поддерживает подобных вызовов. 
  
В следующем примере создается экземпляр **System.Timers.Timer** метода _Startup для формы и обрабатывается асинхронный обратный вызов к таймеру. Кроме того, создается невидимый экземпляр формы Window (**System.Windows.Forms.Form**). По истечении таймера функция обратного вызова выполняется раз в секунду, вызывая функцию Win32 **PostMessage** для размещения сообщения в невидимом окне. Невидимое окно использует функцию **WndProc**, которая обрабатывает сообщение, полученное из функции обратного вызова таймера, и обновляет модель XML DOM для формы. Чтобы эта форма запускалась, она должна быть установлена с полным доверием. Сведения о отладки полностью доверенного шаблона формы см. в обзоре [Preview и Debug Form Templates, которые](how-to-preview-and-debug-form-templates-that-require-full-trust.md)требуют полного доверия. Сведения о развертывании полностью доверенного шаблона форм см. в ссылке [Развертывание шаблонов форм InfoPath с кодом.](how-to-deploy-infopath-form-templates-with-code.md)
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```


