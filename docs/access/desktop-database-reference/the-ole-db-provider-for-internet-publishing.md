---
title: The OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480161"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="18b65-102">The OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="18b65-102">The OLE DB Provider for Internet Publishing</span></span>


<span data-ttu-id="18b65-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18b65-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18b65-104">Объекты ADO [записи](record-object-ado.md) и [потока](stream-object-ado.md) можно использовать с поставщик Microsoft OLE DB для публикации Интернет (публикации Интернета) для доступа и работы с ресурсами, такие как веб-папок или файлов, размещенных в Microsoft FrontPage.</span><span class="sxs-lookup"><span data-stu-id="18b65-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="18b65-105">С помощью ADO можно указать источник **записи**, **потока**или [набора записей](recordset-object-ado.md) URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="18b65-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="18b65-106">Вы можно отправить, загрузить, переместить, скопировать и удаления ресурсов или непосредственного управления свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="18b65-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="18b65-107">Пример кода с помощью **записей** и **потоков** с поставщиком публикации Интернета, содержатся в [Сценарий публикации в Интернете](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="18b65-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="18b65-108">Поставщик публикации Интернет устанавливается вместе с Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="18b65-108">The Internet Publishing Provider is installed with Microsoft Windows 2000.</span></span> <span data-ttu-id="18b65-109">Более ранних версий службу публикации в Интернете, также доступны с помощью Microsoft Office 2000 и Microsoft Internet Explorer версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="18b65-109">Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="18b65-110">Существует три способа подключения ADO службу публикации в Интернете:</span><span class="sxs-lookup"><span data-stu-id="18b65-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="18b65-111">Укажите «URL-адрес =» в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="18b65-111">Specify "URL=" in the connection string.</span></span> <span data-ttu-id="18b65-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="18b65-112">For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="18b65-113">Укажите Msdaipp.dso для *поставщика* ключевое слово строки подключения.</span><span class="sxs-lookup"><span data-stu-id="18b65-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="18b65-114">Пример:</span><span class="sxs-lookup"><span data-stu-id="18b65-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="18b65-115">Укажите Msdaipp.dso для [поставщика](provider-property-ado.md) свойства объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="18b65-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="18b65-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="18b65-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```


> [!NOTE]
> <P><span data-ttu-id="18b65-117">Если Msdaipp.dso явным образом указаны как значение поставщика, с ключевым словом строки подключения <EM>поставщика</EM> или свойство <STRONG>поставщика</STRONG> нельзя использовать «URL-адрес =» в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="18b65-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="18b65-118">В противном случае возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="18b65-118">If you do, an error will occur.</span></span> <span data-ttu-id="18b65-119">Вместо этого просто укажите URL-адрес, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="18b65-119">Instead, simply specify the URL as shown above.</span></span></P>



<span data-ttu-id="18b65-120">Более подробные сведения о поставщике публикации Интернет отображаться [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md)или документации поставщика, входящие в состав исходное приложение, с которым была поставщика OLE DB для публикации Интернет установленные: Windows 2000, Office 2000 или Internet Explorer версии 5.0.</span><span class="sxs-lookup"><span data-stu-id="18b65-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

