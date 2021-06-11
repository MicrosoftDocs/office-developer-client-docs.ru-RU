---
title: InfoPath, кодировка RPC и веб-службы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Веб-службы могут предоставлять один или два стиля привязки к своим веб-методам в контракте WSDL, где они описаны: документальный или RPC.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303530"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="fc28e-103">InfoPath, кодировка RPC и веб-службы</span><span class="sxs-lookup"><span data-stu-id="fc28e-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="fc28e-p101">Веб-службы могут предоставлять один или два стиля привязки к своим веб-методам в контракте WSDL, где они описаны: документальный или RPC. Кроме того, каждый из этих стилей привязки может быть указан как литеральный или закодированный. Самыми распространенными реализациями для каждого типа являются следующие: документальная/литеральная и RPC/закодированная. Однако Microsoft InfoPath поддерживает подключение только к веб-службам, использующим документальный/литеральный стиль.</span><span class="sxs-lookup"><span data-stu-id="fc28e-p101">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC. Additionally, each of these two styles of binding can be specified as either literal or encoded. The most common implementations for each type are: document/literal and RPC/encoded. However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="fc28e-p102">Многие средства развертывания веб-служб располагают переключателем для выбора типа создаваемой веб-службы. При разработке веб-службы, подключение к которой будет выполняться из InfoPath, в качестве стиля и кодирования необходимо указать "документальный/литеральный".</span><span class="sxs-lookup"><span data-stu-id="fc28e-p102">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create. If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="fc28e-110">Однако если над веб-службой контроль не ведется и необходимо подключиться к веб-службе со стилем RPC/закодированный, можно использовать прокси-службу .NET.</span><span class="sxs-lookup"><span data-stu-id="fc28e-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="fc28e-111">Использование прокси-службы .NET для подключения к веб-службе</span><span class="sxs-lookup"><span data-stu-id="fc28e-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="fc28e-p103">Если веб-служба со стилем RPC/закодированный не контролируется, можно создать документальную/литеральную прокси-веб-службу .NET, предоставляющую функции оболочки для каждого веб-метода, который нужно вызвать из веб-службы со стилем RPC/закодированный. После этого с документальной/литеральной прокси-веб-службой можно будет работать из приложения InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fc28e-p103">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service. You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="fc28e-p104">Код .NET Framework может функционировать с любым видом веб-службы (RPC/закодированным и документальным/литеральным), а все веб-службы .NET используют документальный/литеральный стиль и кодирование. Поскольку .NET Framework может взаимодействовать с любой веб-службой, можно создать веб-службу .NET с методами, вызывающими RPC/закодированную веб-службу. Веб-служба .NET будет действовать в качестве преобразователя, позволяющего приложению InfoPath осуществлять вызовы в стиле документальный/литеральный для веб-службы .NET, которая в свою очередь может осуществлять вызовы в стиле RPC/закодированный для исходной веб-службы</span><span class="sxs-lookup"><span data-stu-id="fc28e-p104">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding. Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service. The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="fc28e-p105">Необходимым требованием для создания такой прокси-веб-службы .NET является наличие компьютера с Microsoft Windows или Microsoft Windows Server, где запущены службы Internet Information Services (IIS) и установлена среда ASP.NET. При создании решения InfoPath вместо веб-службы со стилем RPC/закодированный будет указываться прокси-веб-служба. После этого прокси-веб-служба вызовет службу со стилем RPC/закодированный.</span><span class="sxs-lookup"><span data-stu-id="fc28e-p105">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service. When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service. The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="fc28e-120">Создание прокси-веб-службы с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fc28e-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="fc28e-121">Создайте проект **Приложение веб-службы ASP.NET**.</span><span class="sxs-lookup"><span data-stu-id="fc28e-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="fc28e-122">В окне **Обозреватель решений** правой кнопкой мыши щелкните папку **Ссылки** нового проекта, а затем нажмите **Добавить веб-ссылку**.</span><span class="sxs-lookup"><span data-stu-id="fc28e-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="fc28e-123">В диалоговом окне **Добавление веб-ссылки** введите URL-адрес веб-службы со стилем RPC/закодированный, а затем нажмите кнопку **Найти**.</span><span class="sxs-lookup"><span data-stu-id="fc28e-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="fc28e-124">Нажмите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="fc28e-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="fc28e-125">Откройте файл ASMX для веб-службы и добавьте один метод веб-службы для вызова каждого метода веб-службы из указанной веб-службы со стилем RPC/закодированный.</span><span class="sxs-lookup"><span data-stu-id="fc28e-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="fc28e-p106">Для просмотра списка методов на веб-сервере со стилем RPC/закодированный следует открыть окно **Представление классов**. Для каждой веб-службы будет отображено три метода. Например, если метод веб-службы называется  `doSearch`, будет выведено три метода с именами  `doSearch`,  `BegindoSearch` и  `EnddoSearch`. Потребуется лишь создать метод оболочки для метода  `doSearch`. Необходимо обеспечить соответствие точной подписи метода и типа возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fc28e-p106">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window. For each Web Service method, you will see three methods. For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`. You only have to create a wrapper Web Service method for the  `doSearch` method. Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="fc28e-131">В каждом методе оболочки потребуется написать код для вызова веб-службы со стилем RPC/закодированный, на которую добавлена ссылка, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="fc28e-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="fc28e-132">Если необходимо выполнить проверку подлинности веб-службы со стилем RPC/закодированный, можно надежно закодировать учетные данные для подключения к веб-службе со стилем RPC/закодированный в исходном коде для прокси-веб-службы .NET, либо воспользоваться кодом, как в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="fc28e-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="fc28e-133">Дополнительные сведения см. в статье "ИНСТРУКЦИЯ: передача текущих учетных данных в веб-службу ASP.NET" базы знаний Майкрософт по адресу https://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="fc28e-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="fc28e-134">Создание прокси-веб-службы без использования Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="fc28e-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="fc28e-135">В качестве альтернативы для создания прокси-веб-службы используются средства из комплекта разработки программного обеспечения (SDK) .NET Framework, который можно загрузить с веб-сайта MSDN.</span><span class="sxs-lookup"><span data-stu-id="fc28e-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="fc28e-p107">С помощью средства языка описания веб-служб (Wsdl.exe) создайте файл кода для прокси-веб-службы. Файл кода можно скомпилировать, воспользовавшись компилятором командной строки C# (csc.exe) или компилятором командной строки Visual Basic .NET (vbc.exe), которые входят в комплект SDK .NET Framework. После того, как средством языка описания веб-служб будет создан файл кода, измените расширение имени файла на ASMX и откройте файл в любом текстовом редакторе. В самую первую строку документа добавьте следующее объявление:</span><span class="sxs-lookup"><span data-stu-id="fc28e-p107">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service. This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK. After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor. On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="fc28e-p108">Перейдите в конец файла кода и в веб-службе со стилем RPC/закодированный создайте вызов для каждого метода веб-службы. Далее показан образец кода для веб-службы .NET, которая подключается к веб-службе Google, использующей стиль разработки RPC/закодированный. Для расположения сгенерированного кода wsdl.exe существует заполнитель.</span><span class="sxs-lookup"><span data-stu-id="fc28e-p108">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service. The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development. There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


