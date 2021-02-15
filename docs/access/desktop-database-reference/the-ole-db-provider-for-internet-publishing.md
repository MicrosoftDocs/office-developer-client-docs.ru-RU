---
title: The OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314058"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="d0660-102">Поставщик OLE DB для публикации в Интернете</span><span class="sxs-lookup"><span data-stu-id="d0660-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="d0660-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0660-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0660-104">Объекты ADO [Record](record-object-ado.md) и [Stream](stream-object-ado.md) можно использовать с поставщиком Microsoft OLE DB для публикации в Интернете (Internet Publishing Provider) для доступа к ресурсам, таким как веб-папки или файлы, обслуживаемые Microsoft FrontPage, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="d0660-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="d0660-105">С помощью ADO можно указать источник **record,** **Stream** или [Recordset в](recordset-object-ado.md) качестве URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="d0660-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="d0660-106">Затем можно загрузить, скачать, переместить, скопировать и удалить ресурсы или напрямую управлять свойствами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0660-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="d0660-107">Пример кода с использованием **записей** и потоков с поставщиком интернет-публикации см. в сценарии  [публикации в Интернете.](internet-publishing-scenario.md)</span><span class="sxs-lookup"><span data-stu-id="d0660-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="d0660-108">Поставщик публикации в Интернете устанавливается вместе с Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d0660-108">The Internet Publishing Provider is installed with Microsoft Windows 2000.</span></span> <span data-ttu-id="d0660-109">Более ранние версии поставщика интернет-публикации также доступны в Microsoft Office 2000 и Microsoft Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="d0660-109">Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="d0660-110">Существует три способа подключения ADO к поставщику интернет-публикации:</span><span class="sxs-lookup"><span data-stu-id="d0660-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="d0660-111">Укажите "URL=" в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d0660-111">Specify "URL=" in the connection string.</span></span> <span data-ttu-id="d0660-112">Например:</span><span class="sxs-lookup"><span data-stu-id="d0660-112">For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="d0660-113">Укажите Msdaipp.dso для ключевого слова *Provider* строки подключения.</span><span class="sxs-lookup"><span data-stu-id="d0660-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="d0660-114">Например:</span><span class="sxs-lookup"><span data-stu-id="d0660-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="d0660-115">Укажите Msdaipp.dso для свойства [Provider](provider-property-ado.md) объекта [Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d0660-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="d0660-116">Например:</span><span class="sxs-lookup"><span data-stu-id="d0660-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="d0660-117">Если Msdaipp.dso явным образом указан в качестве значения  поставщика с помощью ключевого слова "Строка подключения поставщика" или свойства **Provider,** в строке подключения нельзя использовать "URL=".</span><span class="sxs-lookup"><span data-stu-id="d0660-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="d0660-118">В этом случае произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="d0660-118">If you do, an error will occur.</span></span> <span data-ttu-id="d0660-119">Вместо этого просто укажите URL-адрес, как показано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d0660-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="d0660-120">Дополнительные сведения о поставщике публикации в Интернете см. в документации поставщика [Microsoft OLE DB](microsoft-ole-db-provider-for-internet-publishing.md)для публикации в Интернете или в документации поставщика, предоставленной исходным приложением, с которым установлен поставщик OLE DB для публикации в Интернете: Windows 2000, Office 2000 или Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="d0660-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

