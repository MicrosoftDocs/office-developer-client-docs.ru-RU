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
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a><span data-ttu-id="b8fce-105">Поддержка потоков в проектах InfoPath, использующих объектную модель InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="b8fce-105">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="b8fce-106">COM-объекты, доступ к которым предоставляется через сборки взаимодействия Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll и Microsoft.Office.Interop.InfoPath.Xml.dll, установленные приложением Microsoft InfoPath, не поддерживают вызовы в нескольких потоках.</span><span class="sxs-lookup"><span data-stu-id="b8fce-106">The COM objects accessed through the Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll, and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies installed by Microsoft InfoPath do not support calls made on multiple threads.</span></span> <span data-ttu-id="b8fce-107">Сюда входят интерфейсы для объектов Microsoft XML Core Services (MSXML), заключенные в пространство имен **Microsoft. Office. Interop. InfoPath. SemiTrust** (большинство имен с префиксом иксмлдом) и все интерфейсы, предоставляемые пространством имен [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) , не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b8fce-107">This includes the interfaces for Microsoft XML Core Services (MSXML) objects that are wrapped by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace (most of which have names that are prefixed with IXMLDOM) and all of the interfaces exposed by the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)  namespace, none of which are thread-safe.</span></span> 
  
<span data-ttu-id="b8fce-p103">Все вызовы этих COM-объектов необходимо выполнять в одном потоке. Управляемый код в проекте InfoPath может создавать другие потоки для фоновой работы, но вызовы объектной модели может осуществлять только главный поток.</span><span class="sxs-lookup"><span data-stu-id="b8fce-p103">All calls made to these COM objects must be issued on a single thread. Managed code in an InfoPath project can create other threads to perform background work, but code running on threads other than the main thread cannot call into the InfoPath object models.</span></span>
  
<span data-ttu-id="b8fce-p104">Если в проекте InfoPath с управляемым кодом используется несколько потоков, то следует осторожно распределять объекты между потоками. Нельзя распределять между потоками ссылки на модель XML DOM и ссылки на объекты InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b8fce-p104">If your InfoPath managed code project uses multiple threads, you must be careful about sharing objects between threads. No references to the XML Document Object Model (DOM) or references to InfoPath objects should be shared between threads.</span></span> 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a><span data-ttu-id="b8fce-112">Осуществление асинхронных вызовов объектной модели InfoPath</span><span class="sxs-lookup"><span data-stu-id="b8fce-112">Making Asynchronous Calls to the InfoPath Object Model</span></span>

<span data-ttu-id="b8fce-113">В случаях, когда необходимо вызвать процесс, например таймер, запущенный в отдельном потоке, можно проигнорировать тот факт, что объектная модель InfoPath не поддерживает подобных вызовов.</span><span class="sxs-lookup"><span data-stu-id="b8fce-113">For situations where it is necessary to call into a process such as a timer running on a separate thread, it is possible to work around the fact that the InfoPath object model does not support such calls.</span></span> 
  
<span data-ttu-id="b8fce-114">В следующем примере создается экземпляр **System.Timers.Timer** метода _Startup для формы и обрабатывается асинхронный обратный вызов к таймеру.</span><span class="sxs-lookup"><span data-stu-id="b8fce-114">The following example creates a **System.Timers.Timer** instance in the _Startup method of the form and hooks up an asynchronous callback to the timer.</span></span> <span data-ttu-id="b8fce-115">Кроме того, создается невидимый экземпляр формы Window (**System.Windows.Forms.Form**).</span><span class="sxs-lookup"><span data-stu-id="b8fce-115">In addition, an invisible instance of the window form (**System.Windows.Forms.Form**) is created.</span></span> <span data-ttu-id="b8fce-116">По истечении таймера функция обратного вызова выполняется раз в секунду, вызывая функцию Win32 **PostMessage** для размещения сообщения в невидимом окне.</span><span class="sxs-lookup"><span data-stu-id="b8fce-116">When the timer elapsed callback function executes once per second, it calls into the Win32 **PostMessage** function to post a message to the invisible window.</span></span> <span data-ttu-id="b8fce-117">Невидимое окно использует функцию **WndProc**, которая обрабатывает сообщение, полученное из функции обратного вызова таймера, и обновляет модель XML DOM для формы.</span><span class="sxs-lookup"><span data-stu-id="b8fce-117">The invisible window has a **WndProc** function that processes the message it receives from the timer callback function, and updates the XML document object model (DOM) of the form.</span></span> <span data-ttu-id="b8fce-118">Чтобы эта форма запускалась, она должна быть установлена с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="b8fce-118">This form must be installed as a fully trusted form to run.</span></span> <span data-ttu-id="b8fce-119">Сведения об отладке полностью доверенного шаблона формы можно найти в статье [Просмотр и отладка шаблонов форм, требующих полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="b8fce-119">For information on debugging a fully trusted form template, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> <span data-ttu-id="b8fce-120">Сведения о развертывании шаблона формы с полным доверием можно найти в статье [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="b8fce-120">For information on deploying a fully trusted form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
  
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


